## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:29fd0fea2459ebfcf2a3fb37734c369ef4cb6d867d410f5b60f1f6eabd531f7f
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
$ docker pull buildpack-deps@sha256:cfb53eb38230be3cb01ef9ade4843784a4dd22541d805cdbbe89a043b5d36032
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125856663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877c0e9e2685125a1b6bfd444eda6590d63c41dee63e0fd8361234a637999da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:19:50 GMT
ADD file:3785e6fc0adaed3cfee77ab7dd0756681492573e3553e88b5225fc14d56562d1 in / 
# Thu, 23 Apr 2020 00:19:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:48:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:48:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:48:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91028a6d2ef79dd78d620852cfc6dcda63ffb7301b4a1e87108edd2e9e499625`  
		Last Modified: Thu, 23 Apr 2020 00:24:32 GMT  
		Size: 52.0 MB (51981200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831d9a74fb2992a6446c6eea6a71db00f998b765785b1f37a56464bd43408d09`  
		Last Modified: Thu, 23 Apr 2020 01:01:52 GMT  
		Size: 7.9 MB (7933113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f1160e3e672fe333aee8b37fb0e11661c02ab6ee62a7e276efe6b6f42271d9`  
		Last Modified: Thu, 23 Apr 2020 01:01:53 GMT  
		Size: 10.3 MB (10297877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb1b44c07b5963deefc7eb6049f8d70bbf5144fb469244d7bbc84ab510d03c3`  
		Last Modified: Thu, 23 Apr 2020 01:02:08 GMT  
		Size: 55.6 MB (55644473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c6073963f78fcc0988a4de6bcfa504b3ae047e95f0ef8df9f4f9f43e2c56542b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120681398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6eb5c4339683f696f0aed673231d9a5658e38034b79e8c2a1351552189291aa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:51:06 GMT
ADD file:5be2178df3e21d9545818a91f7ad742ffb521f470db4ffb6f2b4b8e5381d0427 in / 
# Thu, 23 Apr 2020 00:51:09 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:21:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:21:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:22:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07d9742943d725059b0958dfff17760efe7b78df3e20635aab1c80cecf4d1375`  
		Last Modified: Thu, 23 Apr 2020 00:58:41 GMT  
		Size: 49.9 MB (49935576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6804de3a0793db8acc856e22cd4ad64c904053890cc2d87651cc6e49fe02b38`  
		Last Modified: Thu, 23 Apr 2020 01:47:02 GMT  
		Size: 7.5 MB (7514841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270a05b6f98e0c3895a7e4e4a0bc79d3ae0e9198c978423547432797212d3c83`  
		Last Modified: Thu, 23 Apr 2020 01:47:01 GMT  
		Size: 10.0 MB (10008598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f17e3b8b92d507a69bf5d98d8571bbf60bc2f3724064eb6f9dcc64adb3e9a6`  
		Last Modified: Thu, 23 Apr 2020 01:47:29 GMT  
		Size: 53.2 MB (53222383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43e229726ec9f74ce77a889ec8604aa57bf9399be3b04c00f629e1cfe089d440
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115652760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dde45babdfc6349e6ee552bcfcebc76c7d2c759ebb3c5ef5b309af2a070532`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:02:10 GMT
ADD file:85e3bb4657a3517a43e0275a958ad028f3f1684bc8a1a2ab4370553a106583be in / 
# Thu, 23 Apr 2020 01:02:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:584761cab5c57084a1bd0e36523834571e95168e0a6245926b908313dd826549`  
		Last Modified: Thu, 23 Apr 2020 01:10:09 GMT  
		Size: 47.7 MB (47659184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e340b2750c5a3fef5b49207324ded3ab2bab0ec5b13355bc0b1479b14ed1fe`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 7.3 MB (7255985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a158eb7564ad64eba8f5106f2f533b09bdfce834baf124daae77ec75837670`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 9.7 MB (9672905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73dfc1241c0df6667cc7df3946c524d3e6c3ae8ddd128d21feb342d8fa7069`  
		Last Modified: Thu, 23 Apr 2020 04:28:46 GMT  
		Size: 51.1 MB (51064686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0595339a72869a1eaf6ab304752800718e84733b1066727e6b9e60bbfd76e001
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124806275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38d129aa6d1eb15357f7b2a94a7f6c6ad84a44566fad9656b4866512ac46b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:53:05 GMT
ADD file:99275cc5b8d6761ab79ba23a20d3b0bbcf4de8d067f9bfcddaafa88e17896ab0 in / 
# Thu, 23 Apr 2020 00:53:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:33:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 03:34:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66996f8a7f93aa23f91784fa408a35cbaf913d8046e2f6f13a7af916c500e308`  
		Last Modified: Thu, 23 Apr 2020 01:02:28 GMT  
		Size: 50.9 MB (50908186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdfb0684cc2e626db76b396f85933158cbc7dc2b612036dd90856e21e619baa`  
		Last Modified: Thu, 23 Apr 2020 03:50:08 GMT  
		Size: 7.8 MB (7808198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361e10adf6a1fea868c509a1a730cb254017a3f8d82bc5545f885d03eb38e38b`  
		Last Modified: Thu, 23 Apr 2020 03:50:08 GMT  
		Size: 10.3 MB (10294359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1589210a19fdfcc709abcef8745e5944ec6f308c5ec7b7e442e828602914bc02`  
		Last Modified: Thu, 23 Apr 2020 03:50:36 GMT  
		Size: 55.8 MB (55795532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a303993a3bb0c7a379de4a06bdbed195495a884cf4b3975a853196474bb832c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129389060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8da5f15778721d9350fab811b66adc60c0c43235023226378161fbbe44c4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:53 GMT
ADD file:8842691c10d9cacf5f52fd9fdb3b0f3a9a5ed4212d9f2ab558d17e5efd9a758f in / 
# Thu, 23 Apr 2020 00:38:53 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:39:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:40:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bf245c0cdf57ebbfbaf49d796259272bf11094420c0537965c4d322d66b4e55`  
		Last Modified: Thu, 23 Apr 2020 00:43:49 GMT  
		Size: 53.1 MB (53124775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3766da29a92d4e7819901f2cd3fd92af428a41fa1efecc94dadb17f8bd6e6d`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 8.1 MB (8110585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891810791eccf312b55bd366b84147115acf3dc533fd07cc22ed2ce3dd771b1`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 10.7 MB (10657349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b2d4fc44bb2b15f9080c349ce508b8e7c2e640679fb59aaf2f9f78b4b2b456`  
		Last Modified: Thu, 23 Apr 2020 01:58:59 GMT  
		Size: 57.5 MB (57496351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0939b5381ab6e4429f579843e54684e734ede31e0038bb1de713a5ee273043e6
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123065191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabcc2e2701504f3b27aed6c37c8b256414212212c81276f99790c8e9061b6d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:08:38 GMT
ADD file:01a8dba65674c16c3bae58d6e4cf7693a0616ee5efc5495e513ba4454fdaa97b in / 
# Thu, 23 Apr 2020 00:08:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:47:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1ccb563ff5d3d7b0b42a931c0aef1761ab04927c47d729b21ae98a7788ef6af2`  
		Last Modified: Thu, 23 Apr 2020 00:15:41 GMT  
		Size: 50.7 MB (50694211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc1749bc72a1c4ea633b9f43ee46469e3c9b9fca82f799a577fbddf0a0295d`  
		Last Modified: Thu, 23 Apr 2020 01:06:10 GMT  
		Size: 7.5 MB (7460628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed375c9815816af90643e25af4799e3d5c112ac07bc80b13cc5976a394275f53`  
		Last Modified: Thu, 23 Apr 2020 01:06:11 GMT  
		Size: 10.3 MB (10324480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b47876b2590563400c1a797f7f51c2152380cb414e543cb90b037dbd2cee06`  
		Last Modified: Thu, 23 Apr 2020 01:07:06 GMT  
		Size: 54.6 MB (54585872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e570131f196784a19d8d3c757254dfa14e25f3aa3e5f493f7328646aa6bae324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136190022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b3ff5c7610c9cc2c9fa97b0cbce9ed77529245efc3ebe950a5c14ccebfe3b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:32:36 GMT
ADD file:93aa541f8747875de57b6848e6e2df3b2ae7cdc03dcee5489fcfc1bbf45c4920 in / 
# Thu, 23 Apr 2020 00:32:41 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:40:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:41:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23044bc1c77de90086fe2791c49374dbad1ff9af6b3b4dde5f4d46fc92e6a936`  
		Last Modified: Thu, 23 Apr 2020 00:48:13 GMT  
		Size: 55.9 MB (55855771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b244e406f7e60e72181a1fc05e23631e55e349385a03256c692ed685e75d61`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 8.4 MB (8356173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb62044b675b46ae88158a62f5e93b36bed0459b07a8e50881cd48a7d4070e`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 11.0 MB (10975739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3335db3829bab72102f9d1637bea7f1aeb652766860510ad63400bf5e283430`  
		Last Modified: Thu, 23 Apr 2020 02:22:09 GMT  
		Size: 61.0 MB (61002339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2de7ed0cae72a11819d089706d0961b3c507c1e7e8f48c674be9ead54c616d45
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123244519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6143a6db9d555ea14fb4d35ae186866fcc412dd970074183a9941973d649cad2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:50:53 GMT
ADD file:f056a549a046e95dc913639e6f66f03822a0253c29e80ca83bfec0ad17ce61a0 in / 
# Thu, 23 Apr 2020 00:50:56 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:52:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:52:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:53:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dea34220fb3629088500931b5a9b5f42e8310437035ae5d967501a1b59801c6b`  
		Last Modified: Thu, 23 Apr 2020 00:55:22 GMT  
		Size: 50.6 MB (50579994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a059087ed5236381609d7860683f56075adbd498ce096fd21827cb24329124a7`  
		Last Modified: Thu, 23 Apr 2020 02:06:32 GMT  
		Size: 7.6 MB (7600648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb9b52f51c99a0897c6de164eb2fea990a9c6433eb44a6d979eed78270fb2b7`  
		Last Modified: Thu, 23 Apr 2020 02:06:33 GMT  
		Size: 10.2 MB (10183991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65106f2e1ea5731a1e6189fa863014d5706b4d58b8b483e937c817dcd3186786`  
		Last Modified: Thu, 23 Apr 2020 02:06:48 GMT  
		Size: 54.9 MB (54879886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
