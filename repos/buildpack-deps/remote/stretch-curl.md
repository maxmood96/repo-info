## `buildpack-deps:stretch-curl`

```console
$ docker pull buildpack-deps@sha256:ded76113f638c3da4bb15d43c671c9a98eba139032800db823e6fc4f50bcae1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2c63ff29611c794fc8788131d348588b8170f67d00cb64dba38ca9983b6223ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61075716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3434b60e1aea121d1e6631fcd047c7eb390957849552af50a36538ebb189ef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:22:09 GMT
ADD file:ba5db69738244d00088ef591ca43fa8b3189e78fba56bc69b70a232e6f04c7e4 in / 
# Sat, 28 May 2022 01:22:10 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:44:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d3d4e1d44a24e0c5abd41b803d14f211ba153bc7963871713cba8ee5fc687888`  
		Last Modified: Sat, 28 May 2022 01:28:41 GMT  
		Size: 45.4 MB (45429730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec8bceb2e238bbbbec9e458cf83c1342015ed1b717be0f88b50d267c52437d`  
		Last Modified: Sat, 28 May 2022 02:52:34 GMT  
		Size: 11.3 MB (11302994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2aa521faedb4a16c079e9574f537b51a05c2ad4fbabd16f83d9bd58c365bac`  
		Last Modified: Sat, 28 May 2022 02:52:34 GMT  
		Size: 4.3 MB (4342992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7960f9df32a549ef4a2c2263c68561481b5090c76ad5f083288ae933a3503ec4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58639491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f82a9c06e4dc6692bd6be8b95bbd7eadef37d3a050178ff3e2d0a1ef83f8b80`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:08:22 GMT
ADD file:ca5505d9f3e1ac4f55a706fa62d334e14d6bb1ed90bc9b5e693cdbd51baa5450 in / 
# Sat, 28 May 2022 02:08:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:20:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5450f0cf6abbf9c0e24877d991f23d0bb00a7ad2be57f32f1d9a95d1db4d3a6b`  
		Last Modified: Sat, 28 May 2022 02:25:24 GMT  
		Size: 44.1 MB (44124502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47eb48bf728f24b8e81217db5c19aaf41c16e66134d55e1969f52ac53d3e113`  
		Last Modified: Sat, 28 May 2022 03:39:42 GMT  
		Size: 10.4 MB (10352917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18968c0654885075bb50183fe3816b09108c576346ea3b35afdc47af2884a86`  
		Last Modified: Sat, 28 May 2022 03:39:37 GMT  
		Size: 4.2 MB (4162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49f8b10fd848b808f45c7ccc181572edd01378a86039d954ec98774d1ed2f58f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56029573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985c63b1e1bc8a96886c2203a6394e2fc3adb3ee16726b63cb0bb29390a77671`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:05:16 GMT
ADD file:f859825c79355490a08b5fd55799cc3eb1643e21abfeebe59a3a4b08e54e3f7f in / 
# Sat, 28 May 2022 01:05:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:54:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ae3d55ab33f9bf9aa2c47629e66da1c4e679da10d83c29941f39b04140996e4b`  
		Last Modified: Sat, 28 May 2022 01:21:38 GMT  
		Size: 42.2 MB (42150781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277a5551d8d3385d5cf64c67234fe8db9bad96903365595e8c6c61146e48d2b`  
		Last Modified: Sat, 28 May 2022 03:17:39 GMT  
		Size: 10.0 MB (9957035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2055cd14260ece06830786d784271b3008f3ce2ea3279123620a6d78a2afecfa`  
		Last Modified: Sat, 28 May 2022 03:17:36 GMT  
		Size: 3.9 MB (3921757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c0b2ab3ea162f5362f3a6b13228f0b52303fe9874620bfdf4a2301cb4a9ee934
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57304779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a51718560188369c147ff79977c76676a036d09f00389a3be1187ed2ca078e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:08 GMT
ADD file:8949016fba61b18207f5a2309fc974562080c5cc80d1eb82adb35c4fa03f6f05 in / 
# Wed, 11 May 2022 00:49:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:29:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:30:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:139065d8f4553df403babda56f830c32aa1f3e57f18d2145a3179468921a4bb8`  
		Last Modified: Wed, 11 May 2022 00:57:26 GMT  
		Size: 43.2 MB (43212478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0acfd1725613d968a54b7fbfe1f70f24b8a0dad792ad3cb28349035f7736fe`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 10.2 MB (10217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002c314192ef0350d2ac1d1e49b4fddbc49dbcdc609e56e0e2567ee2dd37f0bc`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 3.9 MB (3874525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e76be839adb0272e704625cc931321e6d7a79a42c6609e5ba0ce4990d3c8bfef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61851161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287ce196e68cb8cff0d385e746a2b67f51cb6ea04e99f23e494fe66ab45017df`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:50 GMT
ADD file:1a448f874e606582cb67d9369c97c83c78f2327fde8089b8cb6aaf476dc51935 in / 
# Sat, 28 May 2022 00:41:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:16:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:99b3b0cea6c21e2e36bc4c198a72e5aa3b3ab76d26c2c63d9b0c2b0add554135`  
		Last Modified: Sat, 28 May 2022 00:50:28 GMT  
		Size: 46.2 MB (46150199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cca76d5e15edabc23b8e1a62888ca87b80e71009098aab933b555891ba8af`  
		Last Modified: Sat, 28 May 2022 01:25:03 GMT  
		Size: 11.4 MB (11358709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a795692955c7b33f32b3c1a422a6d1bf8d2d10eea37afa9f414b5ccad00ad0`  
		Last Modified: Sat, 28 May 2022 01:25:00 GMT  
		Size: 4.3 MB (4342253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
