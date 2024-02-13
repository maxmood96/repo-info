## `debian:testing-backports`

```console
$ docker pull debian@sha256:e5f1e8ab996cf7802b723f722bc71b7789ebb96eedb27c6e17d25fda4d9d17a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:56b2dfe33ceb7760e14c2180bed69aa91ef5986b3f7c9be0bc2028c28fa56f79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839855f18533488def76148004e2a8cbed0384df9cd18736910eef02cc69f31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:42 GMT
ADD file:60accd0e24f9359f285bdb996cc23936f5277a33b0c08d9e01c25b16f02e03cf in / 
# Tue, 13 Feb 2024 00:39:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:39:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b1f27ef3dce030fde69c2689259679ae6e799a473bd1aaf174fea653de5b1d6`  
		Last Modified: Tue, 13 Feb 2024 00:45:59 GMT  
		Size: 52.3 MB (52331573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4afbce9358a53369fb89d5ac4b9073fd152b45dd2741b6495e7fe37b9c0b78`  
		Last Modified: Tue, 13 Feb 2024 00:46:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0b639d98cdd3c1c6c0c9e9e9b7d422d7d68bea3a708a178369e4430c60c9ada0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49418619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bc72a549a84c59953a63f399743a9ea09df83397791c1f0a2d4667ab7527f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:10:31 GMT
ADD file:05fe429c75fcd9a35b51e21a4ba1ddd13898be4f8ba5f5f5ec62f2061b2a40ba in / 
# Tue, 13 Feb 2024 01:10:31 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:10:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:934972af2b571c9dd0670c284ab66d94b9c1caebbf237c12931a716256563cb0`  
		Last Modified: Tue, 13 Feb 2024 01:16:42 GMT  
		Size: 49.4 MB (49418396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7520ccc7d267926a2718fc75d38b3f320ef454cf9b46092d1f05e96327ff88`  
		Last Modified: Tue, 13 Feb 2024 01:16:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ab685ab28f0fb9a727e3da60d51d46c60a7257f43e16ac88c49588879194ca94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46914229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae368e657d220a12c9ae8a63cb1f4f3afa179030cf9e757ffeab60c67e9b7c39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:23:33 GMT
ADD file:b17d02e4eb19b8003c005b1828ad7bc6bc0f11f71d3a3e54ac7061e9ed618277 in / 
# Tue, 13 Feb 2024 01:23:33 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:23:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba661c5d3a0b7939175c2dce94119c8ab6155a80d190867e404a6033734e7155`  
		Last Modified: Tue, 13 Feb 2024 01:31:08 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c470a747773e23e9e4a3b84be8daedbce8d457bdac0e421f991ebdf64378cd5`  
		Last Modified: Tue, 13 Feb 2024 01:31:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5b5f238c2cae3472b93f7427732f7bb3f371946aa5ab4c859c341cf15c1126bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52194334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fd6e0d9a4bd458585569c746a8c4156bc7016c0ff9eba2dead3d0d433ba6af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:53 GMT
ADD file:84a74589525ee8c23c5f03b46e981779c3a844eb1650ace0c0f608d665f71690 in / 
# Tue, 13 Feb 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1dd8c22b346593e149ade1aa99ea3d35442a7aa0f7d3e32abb41db5e4ff20379`  
		Last Modified: Tue, 13 Feb 2024 00:48:35 GMT  
		Size: 52.2 MB (52194113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388675718f3fbc308f5c384d8c7464e3927361837375d40c55760c765ce2591a`  
		Last Modified: Tue, 13 Feb 2024 00:48:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:bed41f8338ff6ad75138d04b7c47d3f3d6a7c776e1cb56a11e77fb819aa31f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53167196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e87034d63b8e76cea533df8ab49b3b865259c23f14865fec14ae7bc0eb950`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:24 GMT
ADD file:789c9a55aebcd602f85cbfee8679f0e4818537505e03a39f48f3ef465ff0137c in / 
# Tue, 13 Feb 2024 00:41:25 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2a0cb6457f19e66b6a66209ed9b30d513e33e92a19bb526bdb44b8ffb831891`  
		Last Modified: Tue, 13 Feb 2024 00:48:23 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c84cef52b28da1216af5d4f872d3ca0321f2f4fd6a4e76d7d2f73d1e37ed753`  
		Last Modified: Tue, 13 Feb 2024 00:48:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7870e2989c6c66368db19964ae0976628c737b0c4b45aebea051e78244306d56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51373976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb256628bba1322e3ac36342a83f48703c6906001931c079d6b62d234d4ef96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:44 GMT
ADD file:7af8d4e36ebf06b41ab9afcd5dcc2ab5c14d0342fc0c919c2d4e281a9cd435c7 in / 
# Wed, 31 Jan 2024 22:32:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:33:04 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:912a6e52ac2e7eedcba0446cfc3253750323ce0ce193eb3a3f83d4975425f630`  
		Last Modified: Wed, 31 Jan 2024 22:44:12 GMT  
		Size: 51.4 MB (51373754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9db569d463a1d62614087f7c797773942569b6d277b7dba3ea6c7f15fe1f80`  
		Last Modified: Wed, 31 Jan 2024 22:44:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:fbb4d1c8d740b248e646657aa19ac45349dae7a776682235003388ca348a4511
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56235058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffdc76ab80a7a1fdcc9992d6181cb9071e896fa3a5bf18eaa0e78b6f0ffd7bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:09 GMT
ADD file:fb513218e649a1afb3e363333714c9f9699093574358ac0b47cd3046f1eb5186 in / 
# Tue, 13 Feb 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:17 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26cad4a1d56e1b4700207ff4bc765a669dfe6bc2d3fc942e890febbeec77c519`  
		Last Modified: Tue, 13 Feb 2024 00:47:17 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da256f5abce06773da49df40cd27fa86961f86232856d2451673f9fffc543dd7`  
		Last Modified: Tue, 13 Feb 2024 00:47:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:edf85615f80fb432aba88eac9df601f8e15e3f3b198f8c8e5c2a91f59633a4f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51742543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c41c16f6f0a5763a2e368b0e4713dfba9a3a285db35a3cb36e68f85d42935cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:17:18 GMT
ADD file:9e08f22ce952afa84f6e81b5e9b67fb56721966677cb1078f32490a0caa1fe78 in / 
# Tue, 13 Feb 2024 01:17:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:18:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ee5e82c8f402fc32ba854108be67fb942736c23baf589298d4f94671ddaac35`  
		Last Modified: Tue, 13 Feb 2024 01:32:20 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8b93037e3d277f662dd0217e3339bd8527abf98fe43a3e8538f17b6acf8a3e`  
		Last Modified: Tue, 13 Feb 2024 01:32:25 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
