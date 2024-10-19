## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:498bf9195cd16d43171335249ed823b9c8f5cc4d4dc87423387e6ed7533febc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d3916e45c1b1919b65c5fcf324491e8d1b8c2380f96507ace92275a5723d318b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70842919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e9b58743a7381f5f53c8c6ed89dbf396fe86249f72b153da31e552319b0b28`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad90543a0cace80e4521c0c75ae897cd3bbb6852853f400beb3fed043465ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5490fdfd04a997fdf4839988fcca7e947362a72ef349b49747e39debf5a1e865`

```dockerfile
```

-	Layers:
	-	`sha256:c5efb53970567eaac415d819fedd7e79142f37beb0bb95d76686bed69e20bb95`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 4.5 MB (4492144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3f4bf535ae6901543c9781878d8215d7afa74196a9bdf1873b7512f6d18446`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 6.6 KB (6602 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce982925f7cb662229a416b8ad803c7a5ed65c69917a6fe3e519ac657ba2ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65119280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcde28c3186dce242f6150e5ebe0bb3c3a8f9fe6a7287a3cf88c06f85631668`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9811aa580423a2e552be714c14e210eacb5d77955466d3ca3381faccb47f5832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75437541a1b4d8578a4168a6c973fc1938cef6004aed71846971abe640ce1adb`

```dockerfile
```

-	Layers:
	-	`sha256:ee4e340b3a5aa96d9edd30cd59e56c6a84097292c754303d197005b000003d1e`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 4.5 MB (4493778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc400e038d817658fe4f5c569d165dfce2496c578f62facd784e7288a97c447b`  
		Last Modified: Sat, 19 Oct 2024 00:56:45 GMT  
		Size: 6.7 KB (6656 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ab97857735b9bb4ca0316c84af8cb47f468d79fbf7d69a7602a4a057be20d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69482684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5ace0446f1a3d88fd6d7eb94cc84129b0dc299b80045b5e26f87a3ce7b20b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c985a2a0b84bb74f11845a54a2cf9b51f2f79c056c15b4bd2e136676c9383502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0c728f5437aa596659b21909e26c3dc3ad3d1d64adb107edcf6d718397fc8`

```dockerfile
```

-	Layers:
	-	`sha256:6cfb03deb7abd3faa75a7f964fa9369e9644a2b85204515db2a447c862c83f36`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 4.5 MB (4491756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488572740765c205abccf12b5ac1f0f9f380f18333e681fb042fc29b61ce5b9a`  
		Last Modified: Sat, 19 Oct 2024 01:11:08 GMT  
		Size: 6.7 KB (6676 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fb117244a074d030af0177d95dfa02ae40a9dd404705ec11a8714d6de03266f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb4250e207301019763c2a652f7c0d6950982158eeea54d69191d031358628`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08b4591968723d4d0fdf75817cc1f2f6fbca81c6a5e3e32ce8551977603e00fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb7873e29a676043e203a9f966a180fa83afab781074edefcf1d757c1efeb5c`

```dockerfile
```

-	Layers:
	-	`sha256:7ceec0d5e1bcd10de39b1fab285826c265e8ae4449bc373c17ae99bffd7da1e5`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 4.5 MB (4488583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8a2025755a1ab2cc4010aed335945299dde3703a19af55f8126ca9ac074cd7`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 6.6 KB (6583 bytes)  
		MIME: application/vnd.in-toto+json
