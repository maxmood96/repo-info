## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:81e2e93c6d8db6bb62da858f444e4841e1cd9aea1251e6e0f1910bf8b785cd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:4f40458e9b3d7219323c0f9d148c36f1d400d6384e75db9d6472492708694510
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45377321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e8d9cf4fbcba7e0da003c32b55e6ae3b8d9dce8ad9956cdd5dbaac7caca987`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:22:35 GMT
ADD file:8d2d0b9d4cac88d466d923ea70230b26c3719e5c570c19fa54e18c8cb602893f in / 
# Tue, 17 Nov 2020 20:22:35 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:22:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3fa22b6d826006b1f6df1515426142f63ef33208a1279eb16552686967200a93`  
		Last Modified: Tue, 17 Nov 2020 20:28:42 GMT  
		Size: 45.4 MB (45377097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f79e2cb5c7664e176f86719e6d2d690eedd4d996bf0fedd52802fc942d1660d`  
		Last Modified: Tue, 17 Nov 2020 20:28:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6dd7826ad6050d21186135c1f664c210cc762672199bf4a1d798297a6dab0f11
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44088937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5d19b6497b4493e0d34f0951799f3a6c916f386f1c5839378a50a038ef7ad8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:22:32 GMT
ADD file:cdb0b1bd03aae86c84c89172b03ae6810ecbc3960f24ea871fd56a17faf50e2b in / 
# Tue, 17 Nov 2020 20:22:34 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:22:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f78ba0dc515baa3fc09652a726a3298c8b21f9327fc047d754ece6e2f4bc59e7`  
		Last Modified: Tue, 17 Nov 2020 20:32:20 GMT  
		Size: 44.1 MB (44088712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e9f2f90ad81cdb1c25f604f5df1ddc3e5b1b433be896761301f29c8f360fde`  
		Last Modified: Tue, 17 Nov 2020 20:32:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a02a9276480754f0595de423848c98f52b50e6a20ae7d096497dc27f368500df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ff18d1511aac63b9c6a3f3b56c5ad281681e5786372dfd7fb8b7bcf0f43d14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:08 GMT
ADD file:53daea9b102ac45837a5a6ee26e5380fdd71f29d63e25a456d4b1038d977313f in / 
# Tue, 17 Nov 2020 20:23:10 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:23:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e23d36547faeb615283395692745cf7ca46156dcb237642f63077cf2f14e36d3`  
		Last Modified: Tue, 17 Nov 2020 20:33:27 GMT  
		Size: 42.1 MB (42117769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881942d486978f10ae05b5995fce233e3cbee35614e3b2cd7dacaedb55951cd0`  
		Last Modified: Tue, 17 Nov 2020 20:33:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:09ae41ca4af518075953ded17df0e27c6ec6671ef9d67ca9bdb4a05f7bb45300
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43176264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fa42ef87cf4ead0d867a8391144707fcea4e00e533e927f3df016dcd2a77d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:49 GMT
ADD file:85430081f5ae6632c7127da6405ef907502813b1390576ff2be0aab64de325dd in / 
# Tue, 17 Nov 2020 20:23:55 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:24:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7744bc647d5b0cd976efb3e938567da8bb96e6fcfebac01825e66056bc93df84`  
		Last Modified: Tue, 17 Nov 2020 20:32:23 GMT  
		Size: 43.2 MB (43176036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69b8006bfd44038f08f350c2565a1ec2e5e75b057ea82a8c9ea6aa463cdb308`  
		Last Modified: Tue, 17 Nov 2020 20:32:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:3280d94748d5b29af483c183480c52800825b477e74888cfa989d4db4152f6ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9b8707d6c79f3bf33993c3b375777c806b9c1db8b35e727f9e9ac8aa0d025b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:22 GMT
ADD file:d091db78716dcc7cf61acdbc28f9469aeea357518cd84bbf595a8c1c3209c34e in / 
# Tue, 17 Nov 2020 20:21:23 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:21:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e64c26d7f7907311a434b63c7d584740097deaef61c579cae8c7be9bdc3244b6`  
		Last Modified: Tue, 17 Nov 2020 20:28:17 GMT  
		Size: 46.1 MB (46094829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593d67adb508f82d252db436f9c0862124f875377112646c4c9126b69a08f341`  
		Last Modified: Tue, 17 Nov 2020 20:28:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
