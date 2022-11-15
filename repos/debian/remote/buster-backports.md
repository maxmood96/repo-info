## `debian:buster-backports`

```console
$ docker pull debian@sha256:cf4fc4dbf493add9951b33ca9c3a83e86dae4c65f1ecb3af8be95cf35f727501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:15c37906fab35ab7c75d686caa23fd5af84b7defcae06007ba6b32da8a9dadc4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a706103e88e6ff491a3dbea9d0f87414935a3e5544f2292f3a083c0bae77092f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:03 GMT
ADD file:96ca7e18b6141668321140f8ae1a496641f631313035513f1f9314e9dad2cd71 in / 
# Tue, 15 Nov 2022 04:05:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:05:07 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2730d739afad9b8ff3e3029e23fd69d9533603751d6e42053ce0068c2b58e258`  
		Last Modified: Tue, 15 Nov 2022 04:09:05 GMT  
		Size: 50.4 MB (50448823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a4ba9af6288652cff859ed595f98d015f997aa280ffa425125a2f080fa401`  
		Last Modified: Tue, 15 Nov 2022 04:09:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:38472dc3021912b977564fc0c907477124b896cf787fc431c06e63e11320967e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b0b365db3f1ba6720730055c07c84edfa7c4e193a86b677e3593acfe6f5677`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:39 GMT
ADD file:dd20342abf0e323bf49e7c1f16394f9467c3f5acd35fbae31fc75c86cba3fb75 in / 
# Tue, 15 Nov 2022 03:43:40 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:43:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1a476f56def6dfc092fe7a3c33ef48873726f9a805dbf52045aedcba97457b05`  
		Last Modified: Tue, 15 Nov 2022 03:50:35 GMT  
		Size: 45.9 MB (45915517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433c5518824c4b57f98d6d618dea0b73c1a4fb4b128aa60cfe7e59949b6562a2`  
		Last Modified: Tue, 15 Nov 2022 03:50:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ce9e61651f23da52baccc82e1283504abd8eb18df6dceb1fa92fc954c8a36729
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49234007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec8946d05d31a281563762ec1e1972364cea8561bffca7a5e13c49f0adbe812`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95ba42c648809f33f099f8a6f0f81b1287d5ba05498322d18485d86f07cd3e4`  
		Last Modified: Tue, 15 Nov 2022 01:45:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:444b9a1d964b1f9e91b2e9fadf56259239497144bf26c9065ea460be474e3851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ab75d1d070b7d11d1b50a3d7a72a5823b7c6173e855c764bed9d568e0a517a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:38 GMT
ADD file:e8c5010609ee5ceb22093e461dbe3f9748a4d6ca2fd436e635276b0f99e777e8 in / 
# Tue, 15 Nov 2022 01:41:39 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:46 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a9674eda0741cb717f181697e2f2695ea87fdaf557d253407a096f80ad4f9fb3`  
		Last Modified: Tue, 15 Nov 2022 01:47:27 GMT  
		Size: 51.2 MB (51207653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5563b6f1f70991b2e55043400a3da8e9f259c2c993c0dab6809f29290f545f49`  
		Last Modified: Tue, 15 Nov 2022 01:47:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
