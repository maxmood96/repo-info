## `debian:buster-backports`

```console
$ docker pull debian@sha256:e633da5a76babd21f7153a2167cf3ea61aa74b37fee0f92a11107e9cbc5b636a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:03cdd98519c04765122fe8a5e67a43f52faa286852c4d7d8360eb7b22c205882
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50504243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f066af0c7488a2e5bacc971090e225bf7e5a8c3601d4a5c5955041df277b22`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:51:26 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399abfb6f1bb6546a273e67378b83775defbec3b71faee2d480968e2fbe52471`  
		Last Modified: Wed, 10 Apr 2024 01:56:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:efbfada9e35b6d03c61a591652f5a5127c3b487f7d95f70979eee5ae2b657318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3146eb02cd06bf4a01141d635fc523c70a29ef34783c8a286a6c5263c67cd9b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:59 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
# Wed, 10 Apr 2024 00:59:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:59:06 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd230df8cec635b6851a4b0f3b9daf39f882092eec80ef1ab1665497f9dfaa7f`  
		Last Modified: Wed, 10 Apr 2024 01:05:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:da6afbcbc2ca44ff44ed000572e3d66889d58346e1ab97a2d8547aca0f49daa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c9533971faead9331a12540130b44f652436e25ff378be56c6136b19c2f8d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:40:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363bb358c7f99740f51fd22927236a509120c4fba043ecd1d663ed2bf04c25dc`  
		Last Modified: Wed, 10 Apr 2024 00:45:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4a11c06dbbccaf9e2cc93f1c1c8fb546ad3a6ee65a49502cf1bd257dbf94708d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099f26e6efa04aa872d2bbcebb22f52ff291b63bdc83ab06f9cb6d01afe55b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:45 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Wed, 10 Apr 2024 00:57:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:57:50 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44e05ed9640a63dadaae0b33c5cb22a7a040bf25a00a5060d1fb58e03affb57`  
		Last Modified: Wed, 10 Apr 2024 01:03:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
