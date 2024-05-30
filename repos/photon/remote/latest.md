## `photon:latest`

```console
$ docker pull photon@sha256:6977fe32ca6eb36b41e9185369a3a05fe3053c5c70384596e8189dceb9f17ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:bb1bff167a9bc6891fa826579331322bccdbf079e0ea8d561698bce3d6d427e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16025381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62e800081ccc4ad442972637a0db489e7186b15e2371fa473a1ea0666f13e9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 May 2024 10:45:59 GMT
ADD photon-rootfs-5.0-df154bd74.x86_64.tar.gz / # buildkit
# Sun, 26 May 2024 10:45:59 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240526
# Sun, 26 May 2024 10:45:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:154f0e2d0779506c14ea25bad1d060a0ef516d648bd02fc80d37c227db84be13`  
		Last Modified: Wed, 29 May 2024 20:03:34 GMT  
		Size: 16.0 MB (16025381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `photon:latest` - unknown; unknown

```console
$ docker pull photon@sha256:83b08d96fdd713e28c2e5f597cc4d94909fdae99e4790c3e36f5154bc8471402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 KB (344805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb0aeeb6e2db38ba08df4d3e95cd957ac0a2cfc7e725e3273f093a39a76ed15`

```dockerfile
```

-	Layers:
	-	`sha256:388c9a46c32102ccbe6f851bc758fded37435d785bec8a80035bbbe708524c00`  
		Last Modified: Wed, 29 May 2024 20:03:34 GMT  
		Size: 339.3 KB (339339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60a9502d4308121a8ed352e0dd8d3fdd6f9d849b785536f52b30ee5e254c9452`  
		Last Modified: Wed, 29 May 2024 20:03:34 GMT  
		Size: 5.5 KB (5466 bytes)  
		MIME: application/vnd.in-toto+json

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:4150535cf359b799d10f79ff43a2d5b04a5381e7f990914a7fd1946e34c3f9a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15014932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864a44c7a526a8a7892212ca4077e853f9ca6d97fe1904e4106b41cbb0e80a8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 20:41:25 GMT
ADD file:b2d6d9024ebe077b467abf7a33aee79fef70b719e1a45137c19ea5b24ff57c73 in / 
# Tue, 28 May 2024 20:41:26 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240526
# Tue, 28 May 2024 20:41:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4626c5b0643bebd87363c3243bdb59504c0f703aa8040e05109310406be1a419`  
		Last Modified: Tue, 28 May 2024 20:41:47 GMT  
		Size: 15.0 MB (15014932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
