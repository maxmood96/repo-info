## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:983cf8fdb2f51156184b2846bdda074629fe50be271347da69f6271b1b25673d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3fd4cfe884b2bcbfdbdc950377415e785e9fae378ec9349c62d5eec5a014c52a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed3a0a60d3858457b9a137166a61e1ddf39ffdeb9b1938f38ebb54cac1ac5a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:45 GMT
ADD file:37cd2df02843fb9b61f435e0de74bf98c63d9e85cd586d230064f8616b779bb8 in / 
# Wed, 11 Oct 2023 18:35:46 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:35:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:60fc6018ab9e3056bb7d42b5b77723f444ac5829fa0292ba28019baa6701ff15`  
		Last Modified: Wed, 11 Oct 2023 18:41:20 GMT  
		Size: 50.5 MB (50499408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a98f43dbe9b7b9e27d8101deacc7e94db10913701422a75ca2018028124f21`  
		Last Modified: Wed, 11 Oct 2023 18:41:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0ea482d1b1275d44705ee386890a7e6a6d62a55a6041371a593b2cca1f056eca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce390eb3cb31d3e1e5155657a42bd041b9b48fece81e50c3bb4c042253a6c9f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:56 GMT
ADD file:1317738366a4d06c3f6fa22c055a4f67f7faf1514ab6dd3323566f638199017e in / 
# Wed, 11 Oct 2023 17:42:56 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e9fa2be0c536b2717c1b34816504e850b67315fad7ad009fb7f0ef36a2f52e7`  
		Last Modified: Wed, 11 Oct 2023 17:48:10 GMT  
		Size: 46.0 MB (45966345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c199034c3fa806d7aa62a6e1b4681f0845e03ee57fec77e7accf7d06544e25`  
		Last Modified: Wed, 11 Oct 2023 17:48:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0613c73088f26a40ae6e24ad22a914495be64d469ddd93435ffd47613e784ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6df54ed53101a54830eb679f54d00a8deb97a7f6ab4a226c355016f3292816e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:27 GMT
ADD file:f2dae35ec7eae96132d8191de4e471240d3362635ddc030ff02dd4909ab3cb38 in / 
# Wed, 11 Oct 2023 18:25:28 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:25:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e5effccc364cd39226cd0dc74ba738de8b69df7b99b5281f615e2c00d2cfba19`  
		Last Modified: Wed, 11 Oct 2023 18:30:06 GMT  
		Size: 49.3 MB (49291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93da893f08e91ecd28efc33496754ef54447c3f629e12b287db1abc71ff9beb4`  
		Last Modified: Wed, 11 Oct 2023 18:30:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:55cf6774e1050865f21060601ac5c7d9a4aaae9b4bfb6d469aad4392f2fdbd1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dbad912b73bbb3015137e87d464bb1fb784c85fbf044e88148ea4dddf6e732`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:36 GMT
ADD file:a95fac7e8d4f887905a3b2b79ae5cb6475f961ddff14f2e54997d438d02b170d in / 
# Wed, 11 Oct 2023 17:41:37 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:41:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54e79de8c2b088ec9a4dc8d9a3d3d361812680987bbbf3a12ee529d5e98ed80d`  
		Last Modified: Wed, 11 Oct 2023 17:47:42 GMT  
		Size: 51.3 MB (51256068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f596fae28ada227997705b31b190d2cbb07be89c80c4ab7ffe8effca9b790`  
		Last Modified: Wed, 11 Oct 2023 17:47:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
