## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:a076685449970c3a0a737c8324710ecf87909287853d6030cee5f3e4c1ac573e
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e768b2d73c7da7e7bf0820d432f4b0bbb477d0a47eed00e3080f04cec3d8df64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72411969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd807e1937c65f451ab5e18365c12a8ce841b625344fcec9b9772a483cfafc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:21:27 GMT
ADD file:365db4cb0be9894b5b688c566f8cb6ca848aa3777c680189478799ab75fb4be5 in / 
# Wed, 11 May 2022 01:21:27 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:51:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:51:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cf4cf577d743a8a18a793a3887db0f30d2d2093715da6cdfc0d68ee62f6b790a`  
		Last Modified: Wed, 11 May 2022 01:27:29 GMT  
		Size: 53.1 MB (53147126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1698af61e68ce5cbc91285f790d808bb16bbbb00fbd90de4f2d8ad95bb6d91`  
		Last Modified: Wed, 11 May 2022 01:59:30 GMT  
		Size: 8.0 MB (8000177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7017626ec7dc619c764ea660e0b601241122441e4e77206295325836e01c309`  
		Last Modified: Wed, 11 May 2022 01:59:30 GMT  
		Size: 11.3 MB (11264666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:adfbd512ac7a888d98ac14a454d05d6be7466a786f4a2787b2fa46e2b502a1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69405194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c2836fa7975092971ebed258ec47d10a126dba7fef29b8b0a17993a07f19a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:53:50 GMT
ADD file:4f142f5aefa97fb474a705d0b74abadc5a3efdc7faa28a865e8f774b46affcfa in / 
# Wed, 11 May 2022 00:53:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:15:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1faa3808d790c86a331ed5dce0a7a8af6a26aa395d982f287f5d3fe6362186a`  
		Last Modified: Wed, 11 May 2022 01:10:36 GMT  
		Size: 50.9 MB (50939831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bd191c3a53704df74788d319588194c3f1115cfa7ce0b029d942621a231b1c`  
		Last Modified: Wed, 11 May 2022 02:36:13 GMT  
		Size: 7.5 MB (7537835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8271993242928fca4b8160659ea37b8a1b4a3ca033c568f9e9c1b99e9a9e04`  
		Last Modified: Wed, 11 May 2022 02:36:14 GMT  
		Size: 10.9 MB (10927528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6b362b4d85a0dcd7a5c4ca6c686bfc65074e5230b0d56daf801c7595406b5bf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66520899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384988e3d5bb2977bcf3ccca3d68a0bf9d85e09779bbf535facbdd2ed71945b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:52:42 GMT
ADD file:5256a3df37de011e57faaf3b387bbc66fc94fceb82c48ead6b9e5775cbe7bf21 in / 
# Wed, 11 May 2022 01:52:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:29:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:29:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:528d9ed2cb56db465cbc360f474c45ab8e5ae05c0a0f596fae936fc1290bc68a`  
		Last Modified: Wed, 11 May 2022 02:09:01 GMT  
		Size: 48.7 MB (48678301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d1a1a1705b16f0412d469f63dae500ab636c3d7d35a70874baa189b03a3579`  
		Last Modified: Wed, 11 May 2022 03:52:19 GMT  
		Size: 7.3 MB (7269475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226a116d43744d6f9e056ad8e8a6469b2462f8cc039fafca040cfa47dbf0da1`  
		Last Modified: Wed, 11 May 2022 03:52:20 GMT  
		Size: 10.6 MB (10573123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daaa8deac9e7481f9aa1dde39e8b24eb173d8b5ac927434eecef7816c19506e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71138551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96762db3b73bb30a880f71212110d59cb6085f8d006720c18cb4f3fbe129f9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:48:25 GMT
ADD file:57e11874acd2dc9e0376f854ffe18bfb0b25f8a7a933a3c619d173176c08e412 in / 
# Wed, 11 May 2022 00:48:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:28:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5489557693077b493aaa820cc173d6947baad433930a473cb7cbbb4883ec94f9`  
		Last Modified: Wed, 11 May 2022 00:56:14 GMT  
		Size: 52.2 MB (52242857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b334af1a397894abf6045ff032026c9b4f342acb68ecfe554c22a6f0f272a613`  
		Last Modified: Wed, 11 May 2022 01:38:13 GMT  
		Size: 7.9 MB (7853722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5604865b4585f274eea230691352b972c26efb7b509f1c89ee586a4c6a3559a`  
		Last Modified: Wed, 11 May 2022 01:38:13 GMT  
		Size: 11.0 MB (11041972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8d83e401a946ef10593b07279e1cb695e8d264e6959066b974bcd3446dadea0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75085187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029c77fb24df535a6cd2f3fcece1b20e84f575b296ce9fb568dfb47cab0e00cf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:03 GMT
ADD file:dd10bdbf07bc13b42a7021b48621548cda7b383bf0edb8dff1e35d908f50c392 in / 
# Sat, 28 May 2022 00:41:03 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:14:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e233042357300fc1ac460e8583f90e2b88388d7c2a9016f91be99da315c46fcc`  
		Last Modified: Sat, 28 May 2022 00:49:18 GMT  
		Size: 54.2 MB (54158716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312c6075d7bd54d76868fa2bfad3038339123706e4120edfdacf8be48665b2fa`  
		Last Modified: Sat, 28 May 2022 01:23:48 GMT  
		Size: 9.5 MB (9462060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741e6836ace09c243fa9be77aa56380eeef9635c1dfa4f211ea482b290a4784`  
		Last Modified: Sat, 28 May 2022 01:23:48 GMT  
		Size: 11.5 MB (11464411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:119f4c9f5075b9c54b2dbfa5a67d6fdd14a0d41a18c4112fd7ef361e73bce097
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70794648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698680f024a78155aa775c6203063120bb9713e74201cd48b86d5301cc7813b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:26:20 GMT
ADD file:6fe62ed367eb3d2edf1db05997b04ffb1d77dfe3040a730186cf442070e40212 in / 
# Wed, 11 May 2022 02:26:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:26:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a63c80ef33466ffbd01ed95c3264ba9bdec7ca0346e5abec9019f90436d8ed40`  
		Last Modified: Wed, 11 May 2022 02:36:59 GMT  
		Size: 52.3 MB (52268340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261bd6d6df63a6c5ad11a79cd527284916e16ac0958b840a8df205120e1a1f2`  
		Last Modified: Wed, 11 May 2022 03:43:29 GMT  
		Size: 7.5 MB (7506757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc335614ddc566d478e97b867c18188469549800d7cb2a277186ff09ee59d205`  
		Last Modified: Wed, 11 May 2022 03:43:30 GMT  
		Size: 11.0 MB (11019551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:54d4aba48665731aaa3045cc913cded1066037306bd76c1a00144d50b5b7eab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77910638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3819dec5d06b03e2947d7a6efeb36f5cc2d783ff0e93b848b61f7a0721e0935c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:35:07 GMT
ADD file:7d4f085f5fc874b6142d1d0a27c78512d764e68948baffd110bb6e1ff77c725d in / 
# Wed, 11 May 2022 01:35:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:23:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6f5d4115fab6dd67cca7bafe684609d704cd4e4c3229c7f62f0f1476fe5cfd02`  
		Last Modified: Wed, 11 May 2022 01:45:26 GMT  
		Size: 57.4 MB (57352362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6e8dc2a59c36e07c0ede228c6fdead6ecc03a566fd7328823d686733347f92`  
		Last Modified: Wed, 11 May 2022 03:51:04 GMT  
		Size: 8.5 MB (8492692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348a08a5fd7953090a3d9ecb22bde8041eae82839726dcf3cfccffe516ee74f`  
		Last Modified: Wed, 11 May 2022 03:51:05 GMT  
		Size: 12.1 MB (12065584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:969ab119855ba867ddb6282aec50ff2a1c7e206bdd6f01b15d8b408bf239703e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67286816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292a4ea7f58625b6719107249e9529dec08976e99f7277d5b24ab78b6d7a8597`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:15:02 GMT
ADD file:2406fc75a54a3bdd547095c2a1dba6a536074c482469bd532302201fd8585b5c in / 
# Wed, 11 May 2022 01:15:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:34:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:642ffa8f974e66e7604ce50484153cb3846bd0cb22b2911d01ae5ea68df5291f`  
		Last Modified: Wed, 11 May 2022 01:33:44 GMT  
		Size: 49.4 MB (49377677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b907969c96c55da8d5b6b71e6af3f13438e5d6fdd5dfe41d51bbedd23697a79`  
		Last Modified: Wed, 11 May 2022 03:17:33 GMT  
		Size: 7.3 MB (7258557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d53965d18bb01a1ca71823c7fcbe5f088068e2ef79d5e1c6a55c4d71c5b4e`  
		Last Modified: Wed, 11 May 2022 03:17:35 GMT  
		Size: 10.7 MB (10650582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8205dd707ada9cab83390e5da5ef219881f5e47fb6f33d3cae966eb909b3a1b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70507982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee2327c53a3551ffa5c91fa44a4f11d47292d31f24a1f7f5ae6b5ae64603c97`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:45:28 GMT
ADD file:b2353fefa95af374eef4573e1678567fecc429e2f3c72899f27ecc0dd797bdc6 in / 
# Wed, 11 May 2022 00:45:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:19:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:59733cc7000f12a9b7d5b9dd14702dc414ac30ea3a97284d4693b236ee7f2f9a`  
		Last Modified: Wed, 11 May 2022 00:51:25 GMT  
		Size: 51.7 MB (51687859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d3f87dbb04812d54a2a29118c15b6fef2f06b64013aa102ea2f806405b0492`  
		Last Modified: Wed, 11 May 2022 01:26:32 GMT  
		Size: 7.7 MB (7662400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4ec6bbc903af838f00acaf3d69253b252477fb92dca42c7941cc96e7f6a5fd`  
		Last Modified: Wed, 11 May 2022 01:26:32 GMT  
		Size: 11.2 MB (11157723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
