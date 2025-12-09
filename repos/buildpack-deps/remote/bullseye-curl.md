## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:14b8cbf28c1feea9a588e0dfc5a5b15c38a8c224f4f35a94c5e2b02b1a0b998c
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
$ docker pull buildpack-deps@sha256:468ad2901a9cdbf15bdd4fb9bfba0e4248c99fddbdcbf4b50c3ad06c028ddcc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aa37d28b0d84c4b4f5a3292228bd0c02a719a9c9097613916ec06bd32ca2a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291bf09cec80aaf3d13eefc3fba3a6cb13a44cdce91da75e0e2c3d8b72348e79`  
		Last Modified: Mon, 08 Dec 2025 23:07:20 GMT  
		Size: 15.8 MB (15764219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:771d5f968f446dd9a2e6c7b87a2eba9cf106361bd8b2ff3f6f7039b4abb61f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32877646d6216bc1ef565beb92f6b70ed033386808593e880c60dbe835a1fed1`

```dockerfile
```

-	Layers:
	-	`sha256:8589fa81c27f8e838cf37ca37e376d2289f42506d6c19ea8ac953261f71b6849`  
		Last Modified: Tue, 09 Dec 2025 02:21:06 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9801f0c044b58de10039e6e353e302c97ffcc21eded50ad1b03ad350af5c6c`  
		Last Modified: Tue, 09 Dec 2025 02:21:07 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3d256da522be7179f083e9020640055ab9d70d1f5eb931361d35b466571397da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cac37a051547531ae07ff0ca1b950b6e1b6d35e2fefccfda264ca4dc052b50f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b405dcfbbf208b50f83cb073fc2340dc0c1fad234dcbd26845122feadf5cc1f`  
		Last Modified: Mon, 08 Dec 2025 22:17:00 GMT  
		Size: 49.0 MB (49046374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbf36f43e54145168310c9263866569faa887bc243d2f3bed9e99c1532e0cf`  
		Last Modified: Tue, 09 Dec 2025 00:05:40 GMT  
		Size: 14.9 MB (14879319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce1ac6e6ce07115109fbf5b9520ddcd4e38b46555721647cacee85c256d8096f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb2dfd35d4d0aeda8da4bda790fec4ac78afaee92ec0013c957fdd6e774649`

```dockerfile
```

-	Layers:
	-	`sha256:5403df84e09a244c3a7976846c6ee49106100cefa8661bbf492f5f69788f678e`  
		Last Modified: Tue, 09 Dec 2025 02:21:12 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2197250f22dfe06db0829d41a7b186a306662cc29ac7b40b97f88808c0be3568`  
		Last Modified: Tue, 09 Dec 2025 02:21:13 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4887e66384391210d6eaa122605c2b345970d0c51d3880b57bc910e8cabb9a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68007250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd8ba88ad91d91c4e562e8b8847143b13b397f419578978cbf9fe540fed413d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b879966726dc963ee08cbddddb10287e93034fcf9e3ddf7a290b1b7e42538c`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 15.7 MB (15749537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:022a31f8e25ad32ce4d20b834c344deb1312964c83152aeea1d9c747eced2cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a96943c84e4c0e1120eaf43738380f662c7ab08e459c2aa29234d45041fdbe1`

```dockerfile
```

-	Layers:
	-	`sha256:e72a81459283a2aeebfe77b7976598ed4682e3f9080c6431c5d4c4caa43f7bfd`  
		Last Modified: Tue, 09 Dec 2025 02:21:17 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4dd242f11892ea4c09ad9bd2be79cb279dfb615f70c2c93b8f86c410fb9bd8`  
		Last Modified: Tue, 09 Dec 2025 02:21:18 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:127a90dd16e12bbabbb53f74be5e94a53e5a311231c24dc3509ed930c95fa574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fa7b84364b9a99c68139e8dda5776f402ca8f1a694fcdb55d7e2ffe75df52d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b1d3bd8e8172de52ae5d3823cd522bc420b102de9f2d204bcdd0b93d98aeda`  
		Last Modified: Mon, 08 Dec 2025 23:14:29 GMT  
		Size: 16.3 MB (16267791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4bd01b34ebef18135ff2355ec394cd961b3ac86a7453f8f607b2cf94cb10e926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be082a63d1f80617cd1f6459933ec5d1b758fbb1ea525d24384301112ef0287`

```dockerfile
```

-	Layers:
	-	`sha256:14d37c4cf63339f0a73ec68939f417798d3e707645921517a0f99fd3c7af0816`  
		Last Modified: Tue, 09 Dec 2025 02:21:22 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361a08e1d6047bc513562c5b6e67169a0f5c7abae514731691b7e025e25617ed`  
		Last Modified: Tue, 09 Dec 2025 02:21:23 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
