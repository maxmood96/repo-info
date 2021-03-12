## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:3087b0386ae7e8edd0da609faa5630b596f7ab8b8619e00a47d88d46944918e4
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:65d8a1ac0e1c061002e2c7eed00c0799413a365714139ca187bba11fa2180700
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125406375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ee6e1ffd551bbf88e15ed703c9ddd513715334553d0c3b6725e31156f5f0b2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:04 GMT
ADD file:a858c472d72a55a1ed0b7b2fd2751bac78f77e3549a7533c508022aef7204233 in / 
# Fri, 12 Mar 2021 02:20:04 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:48:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:48:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da21a291c553cde4f403910fa28fb69cad95f63ce1b378f341eb17738b45a6ac`  
		Last Modified: Fri, 12 Mar 2021 02:24:58 GMT  
		Size: 54.8 MB (54835833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f47dd55341835080544d848892987ce23838db35fe64a0d4338b1494ad6ed1c`  
		Last Modified: Fri, 12 Mar 2021 03:17:40 GMT  
		Size: 5.1 MB (5136253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb0644d825d57df2b92d247999a507695a22522c5fa2bd93de229b003ea515b`  
		Last Modified: Fri, 12 Mar 2021 03:17:40 GMT  
		Size: 10.9 MB (10860722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bb105cb94d3a12e9d1648ac4750f9b7b3f837fc623dff8a5676d1892f8ea7b`  
		Last Modified: Fri, 12 Mar 2021 03:18:07 GMT  
		Size: 54.6 MB (54573567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:68a6473bd153d4eb794ca77efd25f192991416fdcea46fde85cc9ced43b541f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b30d1ce138df2932e4646b19d7b138e27ec6c573e3036a3b1033c52c044fa47`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:50:53 GMT
ADD file:d9f9819ac30357029b6474afab9445de462a9c668b49ba4344b2dbaa06df05b2 in / 
# Fri, 12 Mar 2021 01:50:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:58:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:59:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:db47e66a99eee0f0e80fcffdc694f78f48d3211131714143c70983039b44d399`  
		Last Modified: Fri, 12 Mar 2021 02:00:49 GMT  
		Size: 52.4 MB (52366010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ac7c932658262e92ab79badf2b13a9b1cad33b3b58f4142dc86238a03e83da`  
		Last Modified: Fri, 12 Mar 2021 04:16:10 GMT  
		Size: 5.0 MB (5046243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ad2f690c9f36ebf3bd0ddfbb5d3f86e49179efda4e4860ba41f9c421155d95`  
		Last Modified: Fri, 12 Mar 2021 04:16:11 GMT  
		Size: 10.6 MB (10563187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e233f5794bb55dfef65eb8b7574c8c02afbdb36b0c6d8cb233d077183add09`  
		Last Modified: Fri, 12 Mar 2021 04:16:37 GMT  
		Size: 52.3 MB (52315201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49580fefdd803f5a220042bbdc24cc3fa1d2dead00ea210f776b6477c5c70de0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115483129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155479304c87e7ba32e668a0ca1bd8b1e0fc4f6942b9562d9892238cb52e4459`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:58:33 GMT
ADD file:af7fbd0fe0efe7b818f1484ffecc74c401c4d5b949e8e054570ea8cc7a7ed73b in / 
# Fri, 12 Mar 2021 01:58:40 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e093244fe0614201f8731e47ce0387edd785d9fbbe8924f2c8e435a7afabe60`  
		Last Modified: Fri, 12 Mar 2021 02:09:18 GMT  
		Size: 50.0 MB (50033302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66de6d835f521bb9c85648b5a81b3279e777ef73195f17383766d6b48701c5f`  
		Last Modified: Fri, 12 Mar 2021 03:45:35 GMT  
		Size: 4.9 MB (4905657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0b8fc9d72ae8c961878dc03047f7edad8e5025511797effcbca240ae292ee`  
		Last Modified: Fri, 12 Mar 2021 03:45:36 GMT  
		Size: 10.2 MB (10210700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39390d25b386b175cc7e224483f06ef668d193a9ace290ce05b76ec680089826`  
		Last Modified: Fri, 12 Mar 2021 03:45:58 GMT  
		Size: 50.3 MB (50333470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2f43be1b7f7838526097954bf1e85f07dc8face799579bf62862ed8fc40834ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124182083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40e52544647ea29296868ea5dea434c3fa58ef30191d2d9b16420daba220823`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:52:22 GMT
ADD file:0b6f3c6d396337f2754d539814c02240e0a459436f4c0992dabf1736069b5a51 in / 
# Fri, 12 Mar 2021 01:52:29 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:26:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c214bbe001dfa953738440417693c3487f97b371a108bdd62425a704347faf8`  
		Last Modified: Fri, 12 Mar 2021 02:00:33 GMT  
		Size: 53.5 MB (53521132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1332f0d3a2e68785b75d30a2f0eeb7e0902ecf1068899b78d4a7e90f5201cf7f`  
		Last Modified: Fri, 12 Mar 2021 02:42:02 GMT  
		Size: 5.1 MB (5125702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aaac2a7c6ebfc86100e530f2607998a0f8d84b4305495031bbfe789e6e1c2d`  
		Last Modified: Fri, 12 Mar 2021 02:42:03 GMT  
		Size: 10.9 MB (10860189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c201b24dcdc8bd225ab1c164d5ff733c78eb97a701f50d2841449244aa6b43`  
		Last Modified: Fri, 12 Mar 2021 02:42:31 GMT  
		Size: 54.7 MB (54675060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ccc52a7c6629fc99883a3f682a76c0f57da60338f17cf5d90fb424d0980928c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128257123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51d4ce9ec84689d17603a3892ca979b3e89bdc2d75e8ef8496e6907e92ea756`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:43:42 GMT
ADD file:bed5cd029b8a9960b76ca6cc40996e558168731aa38831163dfabe7bda8182fe in / 
# Fri, 12 Mar 2021 01:43:42 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:14:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a9f57a86f966b0edd22e1658988495d14ac0adce930bd6b34f3b6d87ff6e270`  
		Last Modified: Fri, 12 Mar 2021 01:50:43 GMT  
		Size: 55.8 MB (55847447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c33e90bcc52eaf7fb93fd28bda768ee89e08c8939b9086f76ba8159568845e3`  
		Last Modified: Fri, 12 Mar 2021 02:34:41 GMT  
		Size: 5.3 MB (5265242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489d2f5630e3afaad47643cb9f061ff6441e8510705f706d05e12959d9d8e3a`  
		Last Modified: Fri, 12 Mar 2021 02:34:43 GMT  
		Size: 11.2 MB (11240881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cd1263d3b296c32cb3ffdf8344c4fdb870ffa7924132de63c902bf7228f500`  
		Last Modified: Fri, 12 Mar 2021 02:35:11 GMT  
		Size: 55.9 MB (55903553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7b0e4d4b2ff8f56cdaf35dc742241879ef7a1de1a47e4c11a5820af69c3e993b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122366574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233afa7a4b28503f8f266b80db11c9724d8db97cb5873568ad0f156628c6e51c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:08:41 GMT
ADD file:1d48f0f2d8c8cb792d2bbc40d674fcf7f9cd253be061964acd9899304360add2 in / 
# Fri, 12 Mar 2021 02:08:42 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:04:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:04:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a576eefe77178505a1242265c25ca38b94b29862aa56a6bf88c698de0ddc31d`  
		Last Modified: Fri, 12 Mar 2021 02:15:03 GMT  
		Size: 53.1 MB (53092083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4895ee6979d25051187e6c8df7cfcd88bbb3c681b7ce775eb8d68b07962bb`  
		Last Modified: Fri, 12 Mar 2021 03:17:11 GMT  
		Size: 5.1 MB (5098054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dd67088240632fdbd07e5c60a4b7a579388d081a123d8fb5f7522b43d632cc`  
		Last Modified: Fri, 12 Mar 2021 03:17:14 GMT  
		Size: 10.9 MB (10864207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f215da3f5ea6db6eab83dcb3cefed965fd799248492253375df1bd543f463499`  
		Last Modified: Fri, 12 Mar 2021 03:18:05 GMT  
		Size: 53.3 MB (53312230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:24bda25dfa9616ebfa311fdc9a3a7947f753d010a4511317bc3b3098be0aa57b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b83a768c91f2153f3eb92ce205ae12e421810d4c2702330247c85cb1a905f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:30:35 GMT
ADD file:73289d3f358472059064c70edf2135f994f4e4a8ab92fcc0434c1fd611d61e36 in / 
# Fri, 12 Mar 2021 02:30:47 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 10:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 10:38:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 10:43:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eab69212baf77adfba26ada26d0c2b425ac1dd30c3a5bf296485f437993872a2`  
		Last Modified: Fri, 12 Mar 2021 02:40:30 GMT  
		Size: 58.7 MB (58746419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db317d5fedb325c195599b5ae894eac6653f54840383838d929f8320084888f9`  
		Last Modified: Fri, 12 Mar 2021 11:54:21 GMT  
		Size: 5.4 MB (5386575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363f493170adbe10fa914f328698104fa7a698cd4fb5fa4ffe9b3d2f8901354a`  
		Last Modified: Fri, 12 Mar 2021 11:54:28 GMT  
		Size: 11.6 MB (11613810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10460b46a9541b31258ad3baa7c968f5230d30409d3ed9c0dd073edbec01543c`  
		Last Modified: Fri, 12 Mar 2021 11:55:53 GMT  
		Size: 58.8 MB (58847526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a4bfe50d5f6b1e46e09e510650baa58120ee6993df801563395373edd58612f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123029945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ccd88f0ad70037165587d6b64cc373c476ec920d73630206cbde9cc3c2b7d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:06 GMT
ADD file:cb5b3f6c2f66ddb51311634b097823751f759ee3270d06de8388ce763fe1087b in / 
# Fri, 12 Mar 2021 01:45:09 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:28:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cdb5376551135d812bdd513cc33a080cf675d45fd21d8c58d993497afb1e87`  
		Last Modified: Fri, 12 Mar 2021 01:49:44 GMT  
		Size: 53.1 MB (53110995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d00c7fd437d5508e95a96dd508b356303e256508643d5d6fee7c1e90b2aee`  
		Last Modified: Fri, 12 Mar 2021 02:38:37 GMT  
		Size: 5.1 MB (5121380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325387d172e529e98282cbf5484e36eb26e81012e7894300cc43b35dee4780b`  
		Last Modified: Fri, 12 Mar 2021 02:38:37 GMT  
		Size: 10.8 MB (10752500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666766b1f3f8d594995f9643256c8ab2c0b0ac550d63828b195d3594493e457`  
		Last Modified: Fri, 12 Mar 2021 02:38:52 GMT  
		Size: 54.0 MB (54045070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
