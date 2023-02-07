<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230205.0.123931`](#archlinuxbase-202302050123931)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230205.0.123931`](#archlinuxbase-devel-202302050123931)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:a16cb295d8e18778b3263ddb171bb0dacede0faa666f252f7480f89512c09f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c06d6462a83a5b675bb54221e42bc40bbb1914c310323b7eb7f5167d9defa110
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141891914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ee16b66fe81564018ccaf215a72344a616abbd754d5ebc9242a6bc3d8923f3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Jan 2023 20:20:44 GMT
COPY dir:f429cfdbd442f656b5076fe788e2380483244b6b2f043f8605262fb890f0ca20 in / 
# Mon, 30 Jan 2023 20:20:45 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 30 Jan 2023 20:20:45 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 20:20:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7616d49c62052d12e4279524597b528e266dcac352f7aa4ab34deed2e4bf2e04`  
		Last Modified: Mon, 30 Jan 2023 20:22:28 GMT  
		Size: 141.9 MB (141883977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ff5d27d4f6fdaf3a70536c6e506aab9f78d78d68dbcc75d5cfbf5a79c8868`  
		Last Modified: Mon, 30 Jan 2023 20:22:08 GMT  
		Size: 7.9 KB (7937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230205.0.123931`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c1875289de35a3ccc8f3a6cad267a4c64c89187682d6c625569bae05dc53c5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b2c44c9a8b1043e13f62d2399deaa83103e562ba92b34b9dff7d50ae672c0291
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243457694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac286c82a7dadb6a693530902cfb6108e2813e3401b204f814149c18897b494`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Jan 2023 20:21:42 GMT
COPY dir:a195596530c408e680f453591555937d2f1ef5881e7e4de28cb024d6eee48d45 in / 
# Mon, 30 Jan 2023 20:21:45 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 30 Jan 2023 20:21:46 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 20:21:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:558fb3a8d7c6d1bfb0a6619bee47f50c830ccb97975e5763edd9a2f6210c16d4`  
		Last Modified: Mon, 30 Jan 2023 20:23:15 GMT  
		Size: 243.4 MB (243449044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a147ec4744ee4b18ddde59ee6dc1679d3dea3efc9bb7434723f0a198c7f304`  
		Last Modified: Mon, 30 Jan 2023 20:22:40 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230205.0.123931`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a16cb295d8e18778b3263ddb171bb0dacede0faa666f252f7480f89512c09f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c06d6462a83a5b675bb54221e42bc40bbb1914c310323b7eb7f5167d9defa110
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141891914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ee16b66fe81564018ccaf215a72344a616abbd754d5ebc9242a6bc3d8923f3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Jan 2023 20:20:44 GMT
COPY dir:f429cfdbd442f656b5076fe788e2380483244b6b2f043f8605262fb890f0ca20 in / 
# Mon, 30 Jan 2023 20:20:45 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 30 Jan 2023 20:20:45 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 20:20:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7616d49c62052d12e4279524597b528e266dcac352f7aa4ab34deed2e4bf2e04`  
		Last Modified: Mon, 30 Jan 2023 20:22:28 GMT  
		Size: 141.9 MB (141883977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ff5d27d4f6fdaf3a70536c6e506aab9f78d78d68dbcc75d5cfbf5a79c8868`  
		Last Modified: Mon, 30 Jan 2023 20:22:08 GMT  
		Size: 7.9 KB (7937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
