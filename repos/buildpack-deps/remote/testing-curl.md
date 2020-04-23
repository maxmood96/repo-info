## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:1af4a7b884e01e9daafad798c2ef6c4c25b09af380c865afeeac5c8d2dfe2762
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:35e8f0e6033a01ce63f0c950d2b0fd73282a3f5843082d1909336c8482f90af9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70212190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbcf63b251394e7e435345f3714d2982e4ec6a9dceceaa1d5fd5a062eb08ac0`
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

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f035169e1aa3075e61c54ab9eeec0ec229d13fdcadca1b86730a1fc22ef8b7c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67459015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ddb1f41691c7584d0bec633454faa35cdb0d5d334e34c9008d69039eae7494`
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

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:640ececde8ca111411b72daf81768207c4eed9e1ec1757446bfde582c78ffb61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64588074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a4095559e4020c80994ab3ede86fa609a0544d5c72cb148efc300bd455eb72`
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

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7ae26477709b25dd77755162701634e7e9420ea0b2885d41852bcf6baea94d01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69010743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ce3a29efec732c9892e45b5352ccf86a3d6367720067a0d5fc9720b75695f4`
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

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b46cf626b828ef9baff3f7897729f4256351086e25dd7282aacd0b6ed7c518f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71892709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381908f07281083e4b4bf39628b55a05ff23c53221c1461df5bd8d60900eba72`
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

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0746af610bd122b56a89c0777a7e10784799b828900c81e323c0f7b22fdf49c5
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68479319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347c5de411e59953b80101fda57965d324b57e7ca2c3c48f8bb8bbdb492ecb78`
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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:62dfd15aed39d27f89557842e3827bdaeff71805c588dad9ee2eef3412c7d07c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75187683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd193e42bc6cd241e977a911250256e07831d41e980728374a718edbdc34d450`
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

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a13ddb649bf77f0944b0f7589c1e08b71402abe6597a3e6ee9cadd5883289a0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68364633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1769068678f5a7c2f3373dcb187e43c21cb1543b67fb768cc22855d98d835f`
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
