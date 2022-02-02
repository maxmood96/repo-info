## `buildpack-deps:impish-curl`

```console
$ docker pull buildpack-deps@sha256:2ffba8da768d520f0ab6c431798b1c465cf37d5f89b32729076c438ef653ccf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ca18282a2ca61ea2089df473dfd8e96e3bba2e64e8c87f15c26495f5893469bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37623722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4b0bea7729fa2ca38c1bbb9d6e0da6d4902753db9516ff4aaf55d002e8ca46`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:05 GMT
ADD file:16b7fd02fce3322a13d01700f99fe66e6ed2e1973db3361b56f68beb1adccf19 in / 
# Wed, 02 Feb 2022 02:15:06 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 09:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:18:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:24496884391b0c292a71ad3f46bb689ff34f0dee4454901252ba7d52a977bbb0`  
		Last Modified: Tue, 01 Feb 2022 19:45:43 GMT  
		Size: 30.4 MB (30377763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778222c5cf79311601885ba5ac2c44f0ef9dfcd186ef28e0563e6281c2191c4`  
		Last Modified: Wed, 02 Feb 2022 09:38:52 GMT  
		Size: 3.7 MB (3693950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f963dbeca763645c7dbb4b04280642452cc1ea615d22f35dbe1027666dfc08e`  
		Last Modified: Wed, 02 Feb 2022 09:38:52 GMT  
		Size: 3.6 MB (3552009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:84ab522eb782942d421533e83225a7d25d168f5b773a4131104f3bf7419b2395
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34104791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b539be3db00899f718b2203089b6580c273ed704f58487c5e97ea25fb39a2c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:26:01 GMT
ADD file:32cc6b42d18aae85f2e55c58db7c21d70958ea4042c5a3b3d02fa68db5507935 in / 
# Wed, 02 Feb 2022 02:26:02 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:15:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4a304b5b67cb0f88e02dba858b3d63b14bf2910fe10c7ca354d66076202e5a43`  
		Last Modified: Wed, 02 Feb 2022 02:30:44 GMT  
		Size: 26.9 MB (26918632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9de4838f1f90e55ad9c88ab8510ca88acc10d1fda129ced40c0308ef868b78`  
		Last Modified: Wed, 02 Feb 2022 04:48:40 GMT  
		Size: 3.4 MB (3443309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19780ca1848b91057df1dfb6c124559c11d3ca6da5cd58de559a02530a6435ef`  
		Last Modified: Wed, 02 Feb 2022 04:48:39 GMT  
		Size: 3.7 MB (3742850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5696684161153f25a91f40aa5d723b01abcfa34c6c1fa534f5226ffb1bd8e42a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36032745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b360c1393a2666c01d7067ebb420e05d427ad44889b1acf80c56a1d8e34a146`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:46 GMT
ADD file:af631b8d963a33e19a891426c5b4c15e0e884e9b3e5bebf20c2602a8640aa648 in / 
# Wed, 02 Feb 2022 03:19:47 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:18:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:18:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e5a81f6ca6c5971db4a3ff353799dac9a04be755a281494e34ce88fe67356149`  
		Last Modified: Wed, 02 Feb 2022 03:22:01 GMT  
		Size: 29.0 MB (29026521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffbb61d29bef8270c292995b3dd80e5144e5a4d4b1338a0b2ee8aac62fa20cd`  
		Last Modified: Wed, 02 Feb 2022 04:36:55 GMT  
		Size: 3.7 MB (3678893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6dbaef6d25df56d41df9e6b63a20f4af551c84f05741fa0ea2033e63e2da15`  
		Last Modified: Wed, 02 Feb 2022 04:36:55 GMT  
		Size: 3.3 MB (3327331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c06a2079a7f58ee447743252986c3e4d587871cc05254365f0c79775aa348c8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44563556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afef4e50bd8d176a68889e4dc2fecf4c43d42054949967be78b30258c015004e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:51:07 GMT
ADD file:8e3408b07fced25894765792c2a819017c972ca15f54b605b365a78a78b719b9 in / 
# Wed, 02 Feb 2022 03:51:11 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:11:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:37685bfcfd86f994607875169656611b3d61a44ef3aff5a27a2ee9b2a9589d83`  
		Last Modified: Wed, 02 Feb 2022 03:53:55 GMT  
		Size: 36.2 MB (36174678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645f1ef19c3c9982cb00d595afdd4a9918c56afe1ecdbeb41dc7fe949d2c034`  
		Last Modified: Wed, 02 Feb 2022 05:28:17 GMT  
		Size: 4.1 MB (4146831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aaebd659f835776e063ffc0860763d6764b0239ea97ab508dee0f7c2fbc75b`  
		Last Modified: Wed, 02 Feb 2022 05:28:17 GMT  
		Size: 4.2 MB (4242047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:15bfa7410626a506d0af3a81e27c02441d06736b5a7e8146fd9fd6baf02810a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34502633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34dafe44800ec446214234cdd98418fe7196450ddcf55560e2e816c5499d302`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:18:51 GMT
ADD file:aed98a49144458e8d813bb2fe41d35844f33ec0cd407efbbda660d7c4d563ef5 in / 
# Wed, 02 Feb 2022 02:18:52 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:29:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d5ea871c1447312a914987af6fbf45d36b0530a692d2305da1d511d9e26964c1`  
		Last Modified: Wed, 02 Feb 2022 02:38:00 GMT  
		Size: 27.2 MB (27207633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a23d96fb726f08537ef498ee619dd3f58c6aadfc2e5be2db6b4de0582fc6a9`  
		Last Modified: Wed, 02 Feb 2022 04:28:06 GMT  
		Size: 3.5 MB (3490772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938e8ee71b5edd912aad743966cca2640dbf9ecdaa556f981cf3f29855917ca`  
		Last Modified: Wed, 02 Feb 2022 04:28:05 GMT  
		Size: 3.8 MB (3804228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:be076138139172a2962db3ab8b949c4bd732a671618aa971dec33ff59bc2cdbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38257626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c9b221aaed3f1ae8079b03e9dd482d503c492d8ffdef465483a24ed3e23691`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:37 GMT
ADD file:3fe7050ee185df1177ad9379cb909109b7378a099eb79d22193a6156557aadbd in / 
# Wed, 02 Feb 2022 01:42:39 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:12:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:12:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b7789252cadc365c0ef668a46558911d5a49589641581cf378f93ebf7f628cfe`  
		Last Modified: Wed, 02 Feb 2022 01:44:32 GMT  
		Size: 30.5 MB (30526428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7a0349055065a75c3dd86726ee33a39c10307e55f46198783b70736f5d71e9`  
		Last Modified: Wed, 02 Feb 2022 02:20:52 GMT  
		Size: 3.8 MB (3767831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244df8725100b92ceac2f708b84760d1b5ed6d40cfaa3e8c53902b76b2dc4dba`  
		Last Modified: Wed, 02 Feb 2022 02:20:52 GMT  
		Size: 4.0 MB (3963367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
