## `photon:latest`

```console
$ docker pull photon@sha256:a2cc95aa721108dc5f8c9a7670a5cc81733e18105848a412d2780ef88da20426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:6c238d5b44ea038ad1f7f8fbb5a2426cf655a8eaaf8adbb01e86923758437ef4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15909106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db66b214481a66cbe365e77d0b7affb2965dddc3c22616e4a37fcafc0b41870`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 00:19:56 GMT
ADD file:546e9013305af452c699a2779912d005b892184ee8e2558968d0d053ba984269 in / 
# Tue, 23 May 2023 00:19:56 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230522
# Tue, 23 May 2023 00:19:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:21398013bf016dd12b960c38c4dc4eba2cd7e29fc189142e16104ecac9aa7130`  
		Last Modified: Tue, 23 May 2023 00:20:19 GMT  
		Size: 15.9 MB (15909106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:fd412bbcf0ee95048bed9226364f9a257982e24b30d59ce7bd1464fe97aeb040
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14908459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fac23cfc01e0c892555fd0e7c32ddec8849c6bee2efe50fc11e9d15eae694d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 23:39:47 GMT
ADD file:836bd7f3f0587196613fefb91d5f3c5eb86b732002d523aeb22107b6b0368ba0 in / 
# Mon, 22 May 2023 23:39:47 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230522
# Mon, 22 May 2023 23:39:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:129e4ddda07133e7b6b2b8384d17926879656bfe1df545fe0fc1e02326ae12cb`  
		Last Modified: Mon, 22 May 2023 23:40:03 GMT  
		Size: 14.9 MB (14908459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
