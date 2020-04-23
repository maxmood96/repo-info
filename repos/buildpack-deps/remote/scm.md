## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:8424703ba88e2315f47b7ad8d96813e27385d961b6f87a06ead56c05cd5ee54d
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:996e52b4b36754d5f4a69eca558335dab93acd00e4937409443ebe4962cd614e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120018271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23ec82284b583a19ed7134d40ffa68bf65737dd7ddb2703de9a6266ca86a860`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:03f94c32b1a2b9e8c0e25ef3f7bb6bc0c99aa375c0e806bf04823ff1eceb97ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114708383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87fb850675832b6a3b8f0ab9dd89027e655ba27a7fed2cf46cc9bc3248900a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:49:45 GMT
ADD file:1daed63e84abade24fb29c2232024fa993101aafe8a874d4bef96c5635c9ce6e in / 
# Thu, 16 Apr 2020 00:49:48 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:40:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 07:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e139f841569e5d49ea694b0ac42568ff6f00a378e70c53d3153f77487eba09c0`  
		Last Modified: Thu, 16 Apr 2020 00:58:04 GMT  
		Size: 48.1 MB (48096823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e32d16714097e2c6a4b9e2757bc2308e1f2d411ca29c1bf91e72f5a61e587d`  
		Last Modified: Thu, 16 Apr 2020 08:05:33 GMT  
		Size: 7.4 MB (7358957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae86c403d09ed5ec0d2aac79554b33727224226a2329a81ee2ecf02c534aa5b`  
		Last Modified: Thu, 16 Apr 2020 08:05:33 GMT  
		Size: 9.7 MB (9687025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f86ab913051811dbb288b1b8149881c9dfb98b9b98dba2dbd26f6f7ccee378`  
		Last Modified: Thu, 16 Apr 2020 08:06:04 GMT  
		Size: 49.6 MB (49565578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe48f3fcc4161f2991c99a4d51918dbdacb0560b638c5cda081f9f368278cadc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109647997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842b565b25ecaf31c70d97680e2a5bad583150401c73aa7c6492d9fe9442da60`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:59:14 GMT
ADD file:c2369e5669e570f90abaa1fd4fcea4ae1e6654bbd81e8fa070a5b2484c03ee74 in / 
# Thu, 16 Apr 2020 00:59:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:38:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:38:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:39:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:020b29c91094d59c5eb128b7bc2b0b835e2ba4414358664e467428fe8b95bf52`  
		Last Modified: Thu, 16 Apr 2020 01:08:38 GMT  
		Size: 45.9 MB (45864371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f878eece65f73163f26e0755d7bf2d0280b635e9354ee5ac677dd0e1c3b9f485`  
		Last Modified: Thu, 16 Apr 2020 01:56:53 GMT  
		Size: 7.1 MB (7096553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070c5585774beab3cf31d2f66df886bd4295763a00c5f013aab32f261a9559fb`  
		Last Modified: Thu, 16 Apr 2020 01:56:53 GMT  
		Size: 9.3 MB (9343267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e454adb17af2402de86f3b7834eb2d85a7ab8d1199be3963a7ddf802e25a5480`  
		Last Modified: Thu, 16 Apr 2020 01:57:17 GMT  
		Size: 47.3 MB (47343806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:35df78d052ae0b0946f924be1366a1236253e3ba38745a08100146e18a4eda0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118990678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e78c0a35174992b27b59bd5b6f38a7a0cd6c50de5432443679bf6dbd52889ec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:20 GMT
ADD file:02afb66e938cbc67271aaf8cbee75def87458a21d961d02e86383e0ed36b0c71 in / 
# Thu, 16 Apr 2020 02:41:24 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:13:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 03:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d080dad46627d4103daddf54c89f2ef0a0b72ba8270066c50e95ffbf4a79362e`  
		Last Modified: Thu, 16 Apr 2020 02:48:36 GMT  
		Size: 49.2 MB (49169521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8c76f347939ef96b2815e45f9fa43995940a8d4a01525012b2bce1adcbfc3a`  
		Last Modified: Thu, 16 Apr 2020 03:27:53 GMT  
		Size: 7.7 MB (7681332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b6b37aa5fec6dcadc18e45dc6d58e4cf4b967540152c4f44030737e2f5351`  
		Last Modified: Thu, 16 Apr 2020 03:27:53 GMT  
		Size: 10.0 MB (9983908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caa3b2294305ed3cf1d91d1fe2e2dbf3e294a694a4f636dea6bf733975e237a`  
		Last Modified: Thu, 16 Apr 2020 03:28:16 GMT  
		Size: 52.2 MB (52155917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5a119ea7f354719d4704db92e90b664a9dd7752afbaf0845e5a2d0c3bd13502b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122890572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31480e12b660496371aa78347efaf2d1dac7b5f30b81ae1b3bff67f29903ef77`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:37 GMT
ADD file:9a9b9c1d98dfe76e20b3ed67b866e2bdbc1095e26de13b892d07f2a3ee062c83 in / 
# Thu, 16 Apr 2020 01:39:37 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:18:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:19:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a29df432ebf22a237e5e0940a65a1f908be66a5204c5ef240ead7315c27335f`  
		Last Modified: Thu, 16 Apr 2020 01:46:01 GMT  
		Size: 51.1 MB (51147069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec62877ba52bb13d1e47ca6d0c47e1e0d1c61598a0ff5c3590b28c93b2718c3`  
		Last Modified: Thu, 16 Apr 2020 02:37:17 GMT  
		Size: 8.0 MB (7981604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab3373b511919f98b91c8b654596e531ed2f4612bf5b9d63614e0aa420ee01`  
		Last Modified: Thu, 16 Apr 2020 02:37:18 GMT  
		Size: 10.3 MB (10338497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80102fc76b236a12f5fdd11396159f29e8b9567c8c5a159b09b8dc46fc9c003`  
		Last Modified: Thu, 16 Apr 2020 02:37:39 GMT  
		Size: 53.4 MB (53423402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9f796674d151ce2d9fc1864170c1903db315bd9b213aa6c2f1dced01ab0f477e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117103381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8417b67ab188035e5685ff597485d9c22bd7f45ea69ed7c391c91c5083609c99`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:09:25 GMT
ADD file:ef71e7285bfdea3942f5b4db577b5b14ba7dbc37538dfeda1886a6afcef86692 in / 
# Thu, 23 Apr 2020 00:09:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:52:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7754e26af5c07372dee067377cd032efd21a4266d2a432d0bfd78f25f8cb5e64`  
		Last Modified: Thu, 23 Apr 2020 00:17:03 GMT  
		Size: 49.0 MB (49019159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f28a98e4f99b5de98625c7c22aac4386fa49e62ae575a28c1eb055b99d09a5`  
		Last Modified: Thu, 23 Apr 2020 01:09:50 GMT  
		Size: 7.2 MB (7229680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ca975a0efff511dda1467506a9c016219ebcb1621628925ad53008318f87d`  
		Last Modified: Thu, 23 Apr 2020 01:09:51 GMT  
		Size: 10.0 MB (10015780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4bae253397bc57fad0e495b9bf420f3acda3cff409553300952578e291229`  
		Last Modified: Thu, 23 Apr 2020 01:10:46 GMT  
		Size: 50.8 MB (50838762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c31cd9726bcf949c101ac52d8b22869e4dc2e79a2366aec31e674f96f0f49a28
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130571550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fc2ed59efcec764d59f843edb7577e51195f5137de9b4a6fb3043dc2634af8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:37:39 GMT
ADD file:5ea6b62430ec58194ba5685d0b5ecbc2df83c01b4e6c7d8b70f3e96c89390cd5 in / 
# Thu, 16 Apr 2020 01:37:47 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:40:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 05:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:219153a374347511566d1327acf4e45fd3425c20cd49110ef8041930fdb965a4`  
		Last Modified: Thu, 16 Apr 2020 01:53:24 GMT  
		Size: 54.1 MB (54139564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e33f6c16e453e5df771f6cd708cef378a7a3ce2d208a3cce02ff05a4015406`  
		Last Modified: Thu, 16 Apr 2020 06:20:09 GMT  
		Size: 8.3 MB (8252420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7698edca1a58c5374b3f4a126bef6a2d822e931e0c85cd62b78199c597e72`  
		Last Modified: Thu, 16 Apr 2020 06:20:10 GMT  
		Size: 10.7 MB (10727150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a291b3427f488e71a39ecccd11fbbaf98a0e8d552444fbc7db68c1e1f16e3a`  
		Last Modified: Thu, 16 Apr 2020 06:21:11 GMT  
		Size: 57.5 MB (57452416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e869e0adb64b910253dd6808066b06af738b5242c6a4b255298c386453d63fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117595274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6e7ac1c744fc6535921a35d804e0962aeab4380fa2cd8a95441b8feb1e4be7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:03 GMT
ADD file:26367817216af13dc3ba9f495303f7bee8fe138fc8fb728289781563308ce0bd in / 
# Thu, 16 Apr 2020 00:42:05 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:58:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:58:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:59:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54e2fb160a5d4a95ec7efe70c0045923ee557e87ee68ce03f2150b8366f26729`  
		Last Modified: Thu, 16 Apr 2020 00:46:03 GMT  
		Size: 49.0 MB (48960213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f0f1e0f91312a55967b48addc24054fb2e7fb63926a621dd6e86ea62aff2b4`  
		Last Modified: Thu, 16 Apr 2020 02:06:25 GMT  
		Size: 7.4 MB (7382082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ce4aae52f7ba529ea00a3a1bfe7656e52dc1d8b0168a3d70b4e0a4392989f`  
		Last Modified: Thu, 16 Apr 2020 02:06:25 GMT  
		Size: 9.9 MB (9882086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5250b872c2e5d6fcb26d734d43c62187b594e1ce80d34f0cf57fd5e3666b8f`  
		Last Modified: Thu, 16 Apr 2020 02:06:39 GMT  
		Size: 51.4 MB (51370893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
