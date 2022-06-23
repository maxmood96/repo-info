## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:b2ed93a3cdb62c34d1735fe83b1280829ff50f3a34a38046219faac480cc39d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cfd004523264a02f9bc9a39a1a3d6b688e50760b5ad29da12722ee38145ac3df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120138451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6ba92a9dd954ff372c0d595e47d1fd97e03b699e3162c6d0e30f03f513aae3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:51:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014c92148934973210d840dc7cfed53e0afba38d839afaa48ed5150eae19af`  
		Last Modified: Thu, 23 Jun 2022 00:59:51 GMT  
		Size: 7.9 MB (7856631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ff1be7001d642a624409e2d5f90e7708ef7e6f1a75f4eb7362a9296e18d20`  
		Last Modified: Thu, 23 Jun 2022 00:59:50 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e42533e7311ad0a85fe19e9bc5fe3138f608853eeaaea70ee08b2a631b356c3`  
		Last Modified: Thu, 23 Jun 2022 01:00:09 GMT  
		Size: 51.8 MB (51843778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:31cd1aa619edf1c60c0c185601172d6301389fd932ca6059a4d2c059561fd14b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114832726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee179b84db30d7bdee39f7bdf34bf01b49f5f3997af20749714d8548b22a17e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:03:32 GMT
ADD file:ad4ce97f6ea5c59c2f067ac3448d897881ae301cb606e52556637f74cac09774 in / 
# Sat, 28 May 2022 02:03:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:11:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:12:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec27c4ead5d8a5ae35fd4bad58cadacd3d006bed1911fd9b07b5e4f74921f7c9`  
		Last Modified: Sat, 28 May 2022 02:19:24 GMT  
		Size: 48.2 MB (48160631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a992114821be2e9710384caf39f14081084f800a2696a444f4ccbb0b1871735b`  
		Last Modified: Sat, 28 May 2022 03:33:34 GMT  
		Size: 7.4 MB (7400831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07ea5e22b64ba119dfad12a9075a671c03b7ef047af4ba61bc5fd78cd2a0982`  
		Last Modified: Sat, 28 May 2022 03:33:35 GMT  
		Size: 9.7 MB (9687617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c1044d72ac1d1a1dae001eae9012d7d0f660f5a0ce319794ab546237ac3803`  
		Last Modified: Sat, 28 May 2022 03:34:20 GMT  
		Size: 49.6 MB (49583647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d52c0cd23aac62db825d1ea1a4ffa6878e3eb4b21287c57d2cb3a7fd675250d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109764297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928466cc9baeb9bb72f76f9e3d58468301c6b9b041b3a42484c37d60193dc6ce`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:18 GMT
ADD file:3c8ac0c219015f8fbf065e01216d362016d6068cb4e73ea6f0a56893c235a2a7 in / 
# Sat, 28 May 2022 01:00:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:46:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59fe0b97900eb1b641ad94d8d8f3bd9dbff0472e481c4c4c38f2372ef790900a`  
		Last Modified: Sat, 28 May 2022 01:16:20 GMT  
		Size: 45.9 MB (45915564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49649b4a05bcb1345df6dfa9a17fe8f7e713c3a3ff8df5a44f32e7bd74df8bfe`  
		Last Modified: Sat, 28 May 2022 03:11:59 GMT  
		Size: 7.1 MB (7145382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cd2dac771a38a2c51428234f8ad25ae6aa1f7b60d2497c96d251b5fafc88d4`  
		Last Modified: Sat, 28 May 2022 03:11:59 GMT  
		Size: 9.3 MB (9343880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a6a17283b05e5d4fc6748f4fc5c19db1f90640b2e3e18d2b792a6eb338fe11`  
		Last Modified: Sat, 28 May 2022 03:12:43 GMT  
		Size: 47.4 MB (47359471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8081fa196447013b8f21b5da66ce196ad1d54628c4ad3488932a76e701831229
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118891245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2415e4625f37350a99d335b68dd34cd13f8c7a3b912f655a5d67bea730b65ab7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:54 GMT
ADD file:a5e3c0ffa9f9754a6d77fafd8288e699a70f7f6ff7c5912a065f1c69f1393e99 in / 
# Thu, 23 Jun 2022 00:40:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:12:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d6f1451981514e25c21542f5c7ee9bb90052b8856b484ce47294cbf1fd5a234`  
		Last Modified: Thu, 23 Jun 2022 00:47:46 GMT  
		Size: 49.2 MB (49229092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc9fb4baf6e7f2e6ee18ed689c8ee1171c6751c8bbd317d580a193da27a5f1`  
		Last Modified: Thu, 23 Jun 2022 01:23:09 GMT  
		Size: 7.7 MB (7719858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620d55693ed5943ab298346d9ccafefdd6d6f33994e6820a857737df89b65f3a`  
		Last Modified: Thu, 23 Jun 2022 01:23:08 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dcb0fa2b6020cd95c3972ec0fe03da38862f57574fe03a49360713d6f415d6`  
		Last Modified: Thu, 23 Jun 2022 01:23:28 GMT  
		Size: 52.2 MB (52174988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a07cc340bfb318a7918841034e6e09d04d14dabb2f61deae45b393c472836d04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122792545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3e98cb41ebee350997d020be0ed55b12409c5b8d7e70ccd760a75e00b65f0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:44 GMT
ADD file:6437b7652a12d978836b6d8c12403ce48d71210a2944ce96c0ecda8dfd89af2f in / 
# Thu, 23 Jun 2022 00:39:45 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:13:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd723f5696212bd76053aaf0e4dc9c090f488b14b41ae360bafb5574352e90c`  
		Last Modified: Thu, 23 Jun 2022 00:47:04 GMT  
		Size: 51.2 MB (51204247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4827b8abd114ea1d70c6fef5972f989dc7d81f662c584282f4aa12d20703936`  
		Last Modified: Thu, 23 Jun 2022 01:23:31 GMT  
		Size: 8.0 MB (8022623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0f822c867b6ac88f38f1e895c670c32e86a79dd0f62ac9ec5afd6cc3b5eef9`  
		Last Modified: Thu, 23 Jun 2022 01:23:30 GMT  
		Size: 10.1 MB (10122040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49061b906506dd5e7d3e4beaebefeb6ca6446bbdcd913432122e484aadf4dbf`  
		Last Modified: Thu, 23 Jun 2022 01:23:51 GMT  
		Size: 53.4 MB (53443635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f9a52cceab91c5239f79cbdf2cdf184a22c5d6a8128fec2737ee3a9d71babb14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117007838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805510241fb709c471a57bbe173e3f678392e30f470657ccc0af595d4261bd03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:11:47 GMT
ADD file:e86c610403bdbc84066b42627ffdf92eb051badd2f3d1fcc964fba096215c297 in / 
# Sat, 28 May 2022 01:11:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:03:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:03:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ab17b7e8f7dffe546de1529b66b42c5d3aaa0aca409effcd962eae29b834d3e`  
		Last Modified: Sat, 28 May 2022 01:22:17 GMT  
		Size: 49.1 MB (49073373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d8359db5e9434db65ff74cbeb6fb2a3c11834bea89c8bc0c7a81edce49d561`  
		Last Modified: Sat, 28 May 2022 02:27:30 GMT  
		Size: 7.3 MB (7272979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11e4fd36af841919e6113b762dace3a649390107a2ed9224e952e9b71cec164`  
		Last Modified: Sat, 28 May 2022 02:27:30 GMT  
		Size: 9.8 MB (9800289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4e1559e22aa070dc273c40b7ca110c836f73f219de789819c50db5abf12294`  
		Last Modified: Sat, 28 May 2022 02:28:18 GMT  
		Size: 50.9 MB (50861197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c96024628d976e67636f7fc533c08a42224b8a6a7ce24d9851ef86b2bf3668ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130656130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa40aaba206fd73db28d9a25fbf687e6fbf5cc49555ea2de4375fd7c7df29065`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:18 GMT
ADD file:111395200ed598f754f449a2c278d0de3716fe88c66495506bbfba93a1be60d9 in / 
# Sat, 28 May 2022 01:23:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:17:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a84717e4877770b3a8a9f0eb6890cb457d0bf1ec5c2013b56c1a2353beb5cbc0`  
		Last Modified: Sat, 28 May 2022 01:32:57 GMT  
		Size: 54.2 MB (54176994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34161779331d3aba2a35660a49ce70bb924f430f55cd87d24c4a93a50735456`  
		Last Modified: Sat, 28 May 2022 03:37:04 GMT  
		Size: 8.3 MB (8293525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daa1667acca77ec8c0a28fe3d5e8914209d4ab7d21c9ae4f44667705750e5a2`  
		Last Modified: Sat, 28 May 2022 03:37:04 GMT  
		Size: 10.7 MB (10727643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54afe3a1ca9ebf47897da5bf3470187988793f427ac1efc94b7f4d1d754e7db`  
		Last Modified: Sat, 28 May 2022 03:37:27 GMT  
		Size: 57.5 MB (57457968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cd76bcc1cecc0df304ca25714f105dc1d765a61f33bceb8f69e399ab867573fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117696451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b6ad0d61ba5e1e4f6a8caeede5b4788494797b1e015963b82c4848dfa5edd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:20 GMT
ADD file:65712051a170cb9d0b18d0085bc26171598119b8946fa55b5ee959661b48a5d2 in / 
# Sat, 28 May 2022 00:43:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:25:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:771d2d61f47933c8d05a5f7e35dcb16848a6225e7531db8e5971d528982538e9`  
		Last Modified: Sat, 28 May 2022 00:50:02 GMT  
		Size: 49.0 MB (49006810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df770b877bc8966d8f5d52cb3a7ab3f8bbd879f885cd61e637b2561657af7817`  
		Last Modified: Sat, 28 May 2022 02:36:01 GMT  
		Size: 7.4 MB (7423705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfa8ac3a66d83a9351be236e2dad0b6305f4fc7f162891629ed852f205e884e`  
		Last Modified: Sat, 28 May 2022 02:36:01 GMT  
		Size: 9.9 MB (9883325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bc90555bb48ea3318f33a26a32ad4a827ace919e55dd094bd11e93c555a857`  
		Last Modified: Sat, 28 May 2022 02:36:17 GMT  
		Size: 51.4 MB (51382611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
