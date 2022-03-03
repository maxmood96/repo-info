## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:fc17bfcfc7441514bf3bffb9be24c44b66d4b368a22dd182f5da06ee7805ceb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eb05e2752c6ba2ea220cc10a223316de6a1b3e2070934f86dc8bbbcc6031b717
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37910502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caaaababf4ec24596a4954017ff4803e8d415bf2008ee6610f2ef0c6f081d8b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:16 GMT
ADD file:3f673e2aa3a51c7980f0f25985b44578e091d31b3e0a8f481069c20b363a216c in / 
# Wed, 02 Feb 2022 02:15:16 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 09:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:27:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c610536171e3c233fc979d34130a90e9c9bc030425e5af141fd0c3aa8bcf5fb2`  
		Last Modified: Wed, 02 Feb 2022 02:17:11 GMT  
		Size: 30.5 MB (30532381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfc2f9d7d5477c6aededb78ddedb1c8decb0294fbdcbb22d89d3dc0b0551cff`  
		Last Modified: Wed, 02 Feb 2022 09:40:10 GMT  
		Size: 3.8 MB (3818925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a14c37a224f0c145333f74075b0d11d54a5f48d2c2474192e417635a26fb351`  
		Last Modified: Wed, 02 Feb 2022 09:40:09 GMT  
		Size: 3.6 MB (3559196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c6e0dbf8bb446eb535ead89e56831d75d0c61538af864f38766be8e6dd8af1ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34882108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dae089cc017cea453fb241108feb0978575d263f67606fa19c387c121b1d36b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:26:27 GMT
ADD file:b3b2c8a5926e6c518af00fe93b63ed2cd402eaef6cea20252e33036970294826 in / 
# Wed, 02 Feb 2022 02:26:28 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:25:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f5a2de327ec5f0d66e0972ba3099491610a0a555eac3b8beb23e150ad81b1e53`  
		Last Modified: Wed, 02 Feb 2022 02:31:18 GMT  
		Size: 27.6 MB (27599998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ba0d77c40be8b00ac928860b3599cd5f3978a1b462c068142a2be356893624`  
		Last Modified: Wed, 02 Feb 2022 04:52:37 GMT  
		Size: 3.6 MB (3569811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d6f0472085ac38d9c751f76a8d47e2513845c6e30325c5981f26622a4714c`  
		Last Modified: Wed, 02 Feb 2022 04:52:36 GMT  
		Size: 3.7 MB (3712299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dc0f396b22b80c2b89c6079ca31514123c509d1d9e50cbd135ded48d6096ea8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35536397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83145c9e0b9063c2df92a554fadf3ad844988d187e8e97379a3b4636610de67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de81b8d223c70c2ecff8735f6588279de47e4a3c3266d19bf621c5c4ffc048c`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.8 MB (3792303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49986fba69bc0eae7347e2c6882c0b760ce11a31a258fb2694ff83665931577e`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.3 MB (3319390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:aa67988de9c945d43af098efd81e751e68be6eda03fc8d75958d5e409c2af40c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35606791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38da40edb566da21afa7a903982a9781f783e3ef13ef5897738a3c163f499828`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:20:53 GMT
ADD file:b24b04eb8b8b5c5cc58011f4e63b5596c57fa8b6317f8472712142ad1bf70e0c in / 
# Wed, 02 Feb 2022 02:20:55 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5c28c21c482bb799d18f7bcf823f1ac5990e89d600522966a3cf5fe82c052779`  
		Last Modified: Wed, 02 Feb 2022 02:40:32 GMT  
		Size: 28.2 MB (28217972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b251be260817347597a970777f84e0b51e124647e8cea5c780244d783f2916`  
		Last Modified: Wed, 02 Feb 2022 04:37:05 GMT  
		Size: 3.6 MB (3613365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2069686b7922a3f2a8cfad58aed19b9bf47acbe38944df441dc99d25c5108f16`  
		Last Modified: Wed, 02 Feb 2022 04:37:03 GMT  
		Size: 3.8 MB (3775454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:227a9ca4f7e7634e0f05df53b8a07aaf5f9c011350c0a8c0b912a856843de90a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36716040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06f0f392c981b0e8c20ca72f2aadd89672c423204f2c3c2b0276be9dcaaddcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:48 GMT
ADD file:f63d347e51816a3655e11557a605d3c23560bc9478c726a1be3dfc202bba24de in / 
# Wed, 02 Feb 2022 01:42:50 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:14:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:50fdfed8ab37d65d6d796980d94adb16488809e0bd451c26062fec334cbd37fa`  
		Last Modified: Wed, 02 Feb 2022 01:44:45 GMT  
		Size: 29.4 MB (29425828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f6c6fa41b18e9fae55e546bfa9205b25e48dadab0dfb2943b0a5d64f10b263`  
		Last Modified: Wed, 02 Feb 2022 02:21:53 GMT  
		Size: 3.8 MB (3820059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e9f1da527a0c9b5af6226fed9a876b942f1e0ab69894e1a2cec098707c31f`  
		Last Modified: Wed, 02 Feb 2022 02:21:53 GMT  
		Size: 3.5 MB (3470153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
