## `debian:stretch-backports`

```console
$ docker pull debian@sha256:96e0fc5c6ce68f09f72b0d38f2f0073f47e0e2fc927af5192cbf8f2f7b579f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:67b81553bf6a9d199b1b643a5de2b30a2abb090f7799c965a77505894814863e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45367004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85da5d54e71670ef03f44a75a738b7b11b7c124c71eda6eeedb93ee05846e208`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:44:21 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e82c6880dc78f8505175ffce24031776035e0a213f53a667ccc6ac256a44b1`  
		Last Modified: Tue, 13 Oct 2020 01:50:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d96c6ffd378fd0b55d71f23d8b28f72ffc67b5dcf01bd2194d96b91bf2514f51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44081522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2701cbfc5a515049bfe5235b585dc29cb1aff778adaba765a6494ae0652a375`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:58:16 GMT
ADD file:39312a9e824bd7c6ad3eca3ada9e922d8f7219c51e10047672e9ccab3dadb248 in / 
# Wed, 09 Sep 2020 23:58:18 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:58:28 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:301ffd407a7ebea8722c85a0474f1c621b0785275eef7a32a1ab7b5106a8e762`  
		Last Modified: Thu, 10 Sep 2020 00:06:45 GMT  
		Size: 44.1 MB (44081297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da7b2df77b574445a17010dfe1f2c01c71ccee499c0dd6d545696a0463d041a`  
		Last Modified: Thu, 10 Sep 2020 00:06:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fa01f87d7254717d37b1ccddb587301f13bb158f13f0926a49f4f06f853fcbaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42111510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435c9f8cf516b8684930fe2cd3cb7132ee1d58f4dcb6e28738c13d4fefc01da7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:04:04 GMT
ADD file:fb1dab6b0ac08f52870fca9435eedd2f707a3b8a5d28e5d1c2ff88e096f695ec in / 
# Tue, 13 Oct 2020 01:04:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:04:13 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1b636fdf37230c276ff1507a9f2b0067182f369cd669d1852bf5b9f5ba3a43bf`  
		Last Modified: Tue, 13 Oct 2020 01:12:25 GMT  
		Size: 42.1 MB (42111286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d41fe2c9b4f084135e9707ded608f600424ca17158d4ed00cbc06a266692ae4`  
		Last Modified: Tue, 13 Oct 2020 01:12:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1cf223a060c5a759e10c261f6a61648eeadc4f7592b13a58984928dca2313a55
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43171768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b50b0684de9598489f9e986dc4cefdc28668dcff304b17538c70d296a6dad63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:49 GMT
ADD file:2752d391988f4ad7e086be863c36a83a3226e31e44ea816ca4c89d6a410727b1 in / 
# Tue, 13 Oct 2020 01:43:51 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:44:05 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:19e4d0e7f8f2c5cb8a0a8d0e741e9e387c34bd673da69cdcc8e758a5c4dbc106`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 43.2 MB (43171543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dab338b48caac6336869a77ce07c89ff7c619d588cdaad7688e751223af29b`  
		Last Modified: Tue, 13 Oct 2020 01:51:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:0ca1e041768566f9c590494c8ba3c4792ff44c9a6469c797b16c47d702d7724b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46087005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ae2c16fbe806dc3399cce594706798cf98dd27f2e63a055be62a61c2bb25a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:43:30 GMT
ADD file:615d959fea19ddc0e0fd27a59a77c1da8526b37da0b65bae0bfc4aac68c83ad4 in / 
# Wed, 09 Sep 2020 23:43:30 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:43:35 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5147f8567709ad49d5f034aa307bd29bdbbe40bcf438c67f4bc82655742c25c1`  
		Last Modified: Wed, 09 Sep 2020 23:48:59 GMT  
		Size: 46.1 MB (46086780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbf396e5750dd32115852e2fafcf8592af19f9a1becd38ed6b9590f1b29e01d`  
		Last Modified: Wed, 09 Sep 2020 23:49:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
