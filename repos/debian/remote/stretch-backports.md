## `debian:stretch-backports`

```console
$ docker pull debian@sha256:dec61ba59fe94cab3633039634e289f6c82c2aed04d3ee6cdc9ca1342b1a4df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:11b32a17ec309b8e8806286b4b2ed30ec9e26293df1c0fee1a1a8c259197b38c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45381552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8f7ee9751bf1839b11a35bdf17b4c0480c6a610f78869e75b47e495dd68378`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:15:54 GMT
ADD file:23c8493cef4b2584f2526f870645f80d71b4572c29b49a264cea842d2aa2ee28 in / 
# Tue, 01 Mar 2022 02:15:54 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec52bb9d0b765b0726e476d07a8d9b2f808cf7b380f27c1544afa286fe5578cf`  
		Last Modified: Tue, 01 Mar 2022 02:22:47 GMT  
		Size: 45.4 MB (45381330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958937d760a8e3cce4149ccd92bc405172375b0c8d375610d40697bd4ce23586`  
		Last Modified: Tue, 01 Mar 2022 02:23:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:99db07a7ebf38645617f76cd67a41b8f003e429d8b5c0b0a09fe895e890efc95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b6f0d0b6f89ff3bae996b4b0eec897703d25dc21fd999bb843f9486ec7be7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:13 GMT
ADD file:ec0901c267c269fc577d7b4fde4613c524c414738129f0c66a6e4f4939149fa2 in / 
# Tue, 01 Mar 2022 02:08:14 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c2dca75d28e97fb60ac629a75f7314e766bb9e4e8ae03915f095495736fab332`  
		Last Modified: Tue, 01 Mar 2022 02:25:36 GMT  
		Size: 44.1 MB (44091861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdeb470a539e5df43d76b4e4b781ba5cccdd8916aa07a3835f1b1706e242ad57`  
		Last Modified: Tue, 01 Mar 2022 02:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d0304004f01c0c126293efbbb93b018e60e75cdf8a561fc1973ce1c7eab95faa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f93cae8633480115878b573843afe9db8ccea1de1b674c8aa144e9c2d8561`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:52 GMT
ADD file:32b09ecc1f1473cc68b2fe74354febc64a9530d26aa83549020fed06caa8ba8b in / 
# Tue, 01 Mar 2022 02:08:53 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:09:09 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57f32f9fdf459a27691c3a29131c270edd06bf53c003de1f42bb0a6ff8824e31`  
		Last Modified: Tue, 01 Mar 2022 02:25:39 GMT  
		Size: 42.1 MB (42116971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f508ef686f12232ef13c5d07246bba41ef48074e03bb6bd950202d7e7d9a1`  
		Last Modified: Tue, 01 Mar 2022 02:25:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:905bd62ede487a50ae5468cf9bd232d94ec219eb6480f26c99c464d39a955799
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43173963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b825154640b6623d1e841d46cdb663d8bfb744b20b26847e35616dc5a1ae98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:47 GMT
ADD file:2b622f607981bbf2484685f44a5147c3bf81f757fd9129e77f97f72fecc0a0db in / 
# Tue, 01 Mar 2022 02:13:48 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:13:55 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4b9bff972ef4bcbae575403d0d7d36292022bd8d6466c8d00eca1a07d53bb6b2`  
		Last Modified: Tue, 01 Mar 2022 02:22:12 GMT  
		Size: 43.2 MB (43173741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de1f80a687f6665bd21555a0e881c52f4e6b4cc3dea12978915a622b5995ba6`  
		Last Modified: Tue, 01 Mar 2022 02:22:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:2b58bce5fba2fa10ad2f12376c5f49cadef77e02b5ba1f50b501d73d8ba04a89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f34af60fd6104d3389a7a1e10f39cc4c635fa5005ef8fc09a1ecafdf20ab9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:10:13 GMT
ADD file:bc15f0e456e3757963e61c9b01f81ce157b35fb751d837cf7b6ddd9277872821 in / 
# Tue, 01 Mar 2022 02:10:13 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:10:19 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4d460050f4b628f05281226d933aa11a10afffc452771e0d9dd815bb6858e254`  
		Last Modified: Tue, 01 Mar 2022 02:20:11 GMT  
		Size: 46.1 MB (46097796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479f9707514fa875f853ca5c8d47acd6bf9e5e7aef8cc4d0c8e72a853a729b3a`  
		Last Modified: Tue, 01 Mar 2022 02:20:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
