## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:af916acc29830209bf2e71a448508b5611359733c359a1891937d91416140a00
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
$ docker pull buildpack-deps@sha256:94db9f73d597554eba277005a16fd29e8900a71fed7565eb8e5d3e894f830646
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73714307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e104f39111f983109372e979b22697cdb1e50641aff93b683e0670745a0b0b50`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:21:32 GMT
ADD file:dffa51e87e58558bb4b777e117ecb18500d90a9646513d0d8d9724bb5c949dc5 in / 
# Sat, 28 May 2022 01:21:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:43:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7fa02d3fa6e2ab30d6142a096f5321227237c89c02dd890ff9fa745dbf0790d1`  
		Last Modified: Sat, 28 May 2022 01:27:35 GMT  
		Size: 53.2 MB (53161898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0597a54f85d6fe31261321fa5abdce192dd72a61160f5a30e14cfb698b933373`  
		Last Modified: Sat, 28 May 2022 02:51:29 GMT  
		Size: 9.3 MB (9287856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544dfe1044f9dd59f41f2b606fdedfe343ea2f2e7d6ac305fa10a471e369e8c`  
		Last Modified: Sat, 28 May 2022 02:51:29 GMT  
		Size: 11.3 MB (11264553 bytes)  
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
$ docker pull buildpack-deps@sha256:f493ced3cb09b0967a56df698a1e643a06ef3f1d34f9ac6f34be51283dac8382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71957516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6dfdcee79fd862962506058b228c968fc1d0039f292d37c052373a56de6b18`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:06 GMT
ADD file:1687a4039bc00edb9de7ba18be7ce08c7df3d2cf6a4b7a30cb5bb60f41d3c082 in / 
# Sat, 28 May 2022 01:14:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:12:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:13:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a7336e150b70b2115ef0d770279f4e6f79de8d6e16c87dd256445530c1c68d1e`  
		Last Modified: Sat, 28 May 2022 01:24:53 GMT  
		Size: 52.3 MB (52283200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d31486dae68c1e92361c28f610c582d55f682b8dc91e6fadc6ce7d2f167d0f8`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 8.7 MB (8654895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a846f26a733756e5b7a30ab3e72a8147961effdf03d7e9b981808ea3ffc7a6d`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 11.0 MB (11019421 bytes)  
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
$ docker pull buildpack-deps@sha256:90b124d8c81ed2205d915d14d333d12b90e55c3ab54531d92509c4d6e477d3ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68437835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439234e55369bb1f9b3c9f78ca6fc6801cd9f8f3d048cec345ab27214b120138`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:59 GMT
ADD file:e8683ebd7fe3c7f8d36edee19a4eb44173d2c0533a248bb49edfe18fbbec52c4 in / 
# Sat, 28 May 2022 01:15:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:03:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5fcc51d6aaca235d0204fa542679e8c928a4f929dacf2d472c004f8bef16292b`  
		Last Modified: Sat, 28 May 2022 01:33:36 GMT  
		Size: 49.4 MB (49398978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11875dbcf4bf154b85cc0b226364129a3a766fd9696699dece93ac84fc30ecff`  
		Last Modified: Sat, 28 May 2022 02:44:06 GMT  
		Size: 8.4 MB (8388372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcaa3fee1a4ad6e285aa0e16f72b33694c419b2821bdeec5341875dc49f47c6`  
		Last Modified: Sat, 28 May 2022 02:44:07 GMT  
		Size: 10.7 MB (10650485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0ace02333ed9a186b42d07023833d74346d1c92b6a95ba54895d49161bae46b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71799721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda910f1787d0740cdcc32ff6fce4a669e003118fd313a92e8c6545fff41f79b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:44:37 GMT
ADD file:03a528116badd98d1660ab1a83ce0462a11168a2dae972be4891032c54483f22 in / 
# Sat, 28 May 2022 00:44:41 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:28:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0cf941fb152b37e3fda284ae5eceb3dab36c26511fe06a7105ee43081ca68554`  
		Last Modified: Sat, 28 May 2022 00:51:02 GMT  
		Size: 51.7 MB (51703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ecd77e960fd212da3eca4e59b9c918e4d7af7e1ea705150c26c05f5967f79`  
		Last Modified: Sat, 28 May 2022 02:36:52 GMT  
		Size: 8.9 MB (8938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6e701baf55072de709e3a913641d40af39439387278f3abde5d58deb12714`  
		Last Modified: Sat, 28 May 2022 02:36:52 GMT  
		Size: 11.2 MB (11157585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
