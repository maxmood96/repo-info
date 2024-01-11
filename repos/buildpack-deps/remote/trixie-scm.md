## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:fe8fc08af46dcc82239c5a34f92dcac640f8cb66a5c01ff1aae11ad15641170a
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f95118a633c5251d720d361a6e57122041e3fe2e38daa37ad524208f40959958
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142070908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fe5e209c24b14c22a80d671f7f8ba544cd6db8d8e233b347c1ec26ea271947`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:38 GMT
ADD file:221c5996f1ff4dd71764ca719f363e27bb329a807e397f6654cbb3c478c54c9e in / 
# Thu, 11 Jan 2024 02:40:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:42:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5c06b5f92f5d425b6a1eca65d06813d5da1bf325255b6cdab64db03a7ee0d47`  
		Last Modified: Thu, 11 Jan 2024 02:47:11 GMT  
		Size: 49.6 MB (49562052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b14ab6cee5b8a008ac52067ba895976219bd813b8d4aa739a74ba5ce9121594`  
		Last Modified: Thu, 11 Jan 2024 04:48:48 GMT  
		Size: 26.5 MB (26464231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e1dd418040b8206f8c9d1069566b49a386b6b9fc3cd2fa8612d76819d240e3`  
		Last Modified: Thu, 11 Jan 2024 04:49:06 GMT  
		Size: 66.0 MB (66044625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6a8a8ec1634be1994e0f16ac1f344117cddb5dff89654916fffccc8eec1f1194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135894177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05d4ab7fb5379a220ec41e32f8b0db52575325dadcec990b0b36fd871ac7c06`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:51:35 GMT
ADD file:406477db7977cf7bae3dd986446192c7a9c9187721f800f6414add12009ed4fd in / 
# Thu, 11 Jan 2024 01:51:35 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:02:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:03:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ffe09ad7d6788d69349e61610eec99edf75d529a8f29e51e982f323dd5b39a9`  
		Last Modified: Thu, 11 Jan 2024 01:57:42 GMT  
		Size: 47.3 MB (47275273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbe43ce8740ef7b4c0109654d60ec4abac22aef1e893ddf0a49dc137bd8ece`  
		Last Modified: Thu, 11 Jan 2024 07:09:58 GMT  
		Size: 24.9 MB (24928594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b219cbdc80fe84c71063f1130563a61cbc3acadd8af61e3506e813ebe8344`  
		Last Modified: Thu, 11 Jan 2024 07:10:22 GMT  
		Size: 63.7 MB (63690310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c62633741594b3679dd8a8d5c9780b064eb85477a99348edcb2f3c955dcff4e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130223123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f44348367d2d0f0ae98dede80947e6508caacb2f22eeb3b0bf46ddd0098790`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:45:43 GMT
ADD file:2578bbd6242f569b630ed2a8dbbe60a6317a1fd910aebe4814313b4c0eb7a482 in / 
# Thu, 11 Jan 2024 02:45:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:25:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d77eb11f48fd53e8f4a4cad655e31f2fb5f91177fb35abe347a055a3352eff1b`  
		Last Modified: Thu, 11 Jan 2024 02:53:33 GMT  
		Size: 45.1 MB (45063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37916331c99d3b698aae6553fb6c2a2c76d2cdb8dea2d3cc6e825c690f03420`  
		Last Modified: Thu, 11 Jan 2024 03:34:33 GMT  
		Size: 24.1 MB (24103233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb41fed208e1ec1bace230d40b75cf9e9012e2296ace322150b1ff2f121346`  
		Last Modified: Thu, 11 Jan 2024 03:34:58 GMT  
		Size: 61.1 MB (61056442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7443aa357286ae7203b3ba04995c65200a99c65010153e6c569a50f462ae629b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141771554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be66e45e142b694933001f1b8319e3866a1f841c759af4cd48af707b34384362`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:31 GMT
ADD file:8d6ad5a2ffd09b80912ad6e70510597c7fc97adbf4f68d39203c3711ddb56a51 in / 
# Thu, 11 Jan 2024 02:42:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:32:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5d062756698b7a985fb1a991d4720ffd4d0a2a6c27002bf3939d178a81e7024`  
		Last Modified: Thu, 11 Jan 2024 02:48:34 GMT  
		Size: 49.6 MB (49594187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0407b18fc98c19c25cb39b17797717f780dc263659c85f55c6b854e1b6aab7d3`  
		Last Modified: Thu, 11 Jan 2024 09:37:41 GMT  
		Size: 26.0 MB (26014238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03554a7182e2bf0ab5f3b345f0f76d47f2c2a49f7a49bacf09ff87268640dea2`  
		Last Modified: Thu, 11 Jan 2024 09:37:57 GMT  
		Size: 66.2 MB (66163129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4a295dfe4fa14020a6ecb1c175ad0ec3a8b1b91cb3e6e7b57f498443a92068f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145795685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c6f3a6839606d20158ce1444c93c6509f863305bb88fd087bb64aeb28538bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:24 GMT
ADD file:5564e4ab4c2aca360aa2b99bcb8c9c77e6d97554833ae3cc9bb2f49ed35e25b2 in / 
# Thu, 11 Jan 2024 02:41:24 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a827afb392949e39b5beea804bcbbd7be98a07848f45ead6a59e020bce5836dc`  
		Last Modified: Thu, 11 Jan 2024 02:48:52 GMT  
		Size: 50.5 MB (50527068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181d3088fd6488ff4296a6d76024c5ceabebb089069d60b6dcbf62cc62624985`  
		Last Modified: Thu, 11 Jan 2024 04:47:28 GMT  
		Size: 27.5 MB (27453882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f427ac95ec51ede300e74262c9ded6e199d3947a3341d21a1dc672fb66a3c458`  
		Last Modified: Thu, 11 Jan 2024 04:47:52 GMT  
		Size: 67.8 MB (67814735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5e6682897347e0d3203ed2b317c0724c33182d531ece32000b599a3a88d89437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140460648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e22dd3175826b1a60cd4e27487bcb5e853314cf2e341afd441eb5d19a55965`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:18:24 GMT
ADD file:f8968c17bd3825e4f058fd68c683a3c699e06368b69577a14d575a0c3ac70e6c in / 
# Thu, 11 Jan 2024 02:18:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:17:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc5cc64b8a2f7c7d0c78917ac707955e566c39f9c62003870eb7cd32f7b23a5f`  
		Last Modified: Thu, 11 Jan 2024 02:30:01 GMT  
		Size: 49.3 MB (49333270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136a6eeb1b81bae44e0e846833442693a689a375fce576961be0a2c167f5f861`  
		Last Modified: Thu, 11 Jan 2024 03:34:44 GMT  
		Size: 26.2 MB (26204931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bb2f97a9c0cb49fd93afb006f99f7d60718b4032952d234bb51636d62c2ba0`  
		Last Modified: Thu, 11 Jan 2024 03:35:36 GMT  
		Size: 64.9 MB (64922447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:088adc08b641082ed9c976b639d8895fe146149949a1d0e5803e35bdbe5d35f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153951770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae5de4cab4759ba9c2128e548780de25ca47d26ac151b8fd57763714978e487`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:16 GMT
ADD file:d68448f447d4318f3f9fad32f62806e0a419160a92848f345b24ec3a1aa68cf9 in / 
# Thu, 11 Jan 2024 02:37:19 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:451fd7c87652550c3d81b74039588f9cc1098943015d72618adc689c50a31de3`  
		Last Modified: Thu, 11 Jan 2024 02:43:06 GMT  
		Size: 53.4 MB (53435762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721dab59d6faf980a2731617cf00ce4d4f5118003d8d0c3dad0ce0ff7844f94`  
		Last Modified: Thu, 11 Jan 2024 07:27:03 GMT  
		Size: 29.0 MB (28965246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4760a29b48a1de750877fea0b09353ed2b9b3a55427381e4cca70f8fb2bc47df`  
		Last Modified: Thu, 11 Jan 2024 07:27:23 GMT  
		Size: 71.6 MB (71550762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e516683398caf40a91e9cd0008c18275d038e56eff73145f666459597a76763b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143422544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c23bb2a09d15bf9e700a51e20877dc7eaf60be1436b45caec9898723d47a2dd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:25 GMT
ADD file:3ce2a6c625c267468f6ecc7899fd855c1705b7efb767d466e8b5e859b1047897 in / 
# Thu, 11 Jan 2024 01:48:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:15:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c1c69c5e90f50e1791d192ea58f134dbc8ecc231a5b815d4c7ee99ef3a1ff7`  
		Last Modified: Thu, 11 Jan 2024 01:53:03 GMT  
		Size: 49.1 MB (49091863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3694e83d440b396cbb77938e6510f4437f21e56dc3bfaed630e6caab9214d`  
		Last Modified: Thu, 11 Jan 2024 02:23:52 GMT  
		Size: 27.2 MB (27199817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47161a7187326816c278e7d750ac894a70682803dc239b5d8c20d926e36e792`  
		Last Modified: Thu, 11 Jan 2024 02:24:08 GMT  
		Size: 67.1 MB (67130864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
