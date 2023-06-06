## `fedora:rawhide`

```console
$ docker pull fedora@sha256:78c8f111a898e239660961ba0815782a866e55c3b88e5478e8b423e0872bf0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:649ec5c98d263f3cfeb4be02630ddbe7492f967f997986fa2706e83f5ccf6a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68469901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e956bfeffc9c7a602b1c4d1f18a983d705ad673ba66a4f4e099e777279cf5b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:20:05 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 20:20:17 GMT
ADD file:190f7eebffe7e3a50b341655317071726e82b8560aba1fdc0105e109a3275ad4 in / 
# Tue, 06 Jun 2023 20:20:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:83fb1a35b0ac26949417f38861aa80a70cd9d9ddc63ab13bc11f20c9365f7456`  
		Last Modified: Tue, 06 Jun 2023 20:21:09 GMT  
		Size: 68.5 MB (68469901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:9e726e3052bdb633096b4d84f9d29082aac3def4f630c5ce6226b166c226f144
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67205357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d46dac57db33f4823ff624d7187f37a3d7e0a619a03a5e693696b1b0fffd524`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:39:50 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 19:40:14 GMT
ADD file:3e6cf1e39ef84e98a1b3dfd08275fc07a29f0d898d30849b178d0c04bfad21fd in / 
# Tue, 06 Jun 2023 19:40:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91dc871cee77c64af13bb6bc2db01ef886031f113319c4c7393546f649f420d7`  
		Last Modified: Tue, 06 Jun 2023 19:41:00 GMT  
		Size: 67.2 MB (67205357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:4c67fe09823af16107abbed153250649f5dc9db7c1ae15115ea6a1a5cc9f8c42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75132944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e49f96d77faee9414ff7290bf5d4f00c528e5281a60dfc0a6ae8d2fa4b78b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:18:04 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 20:18:05 GMT
ADD file:dd1a39c61dcc82b463d39baeca4f2b8ddce1f438a841ddc889993f7c4e19d687 in / 
# Tue, 06 Jun 2023 20:18:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f83bdc4847e939bcfcde5a295a0d2f495e047e37f70ecf8b4872d75719ebb12e`  
		Last Modified: Tue, 06 Jun 2023 20:19:32 GMT  
		Size: 75.1 MB (75132944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:becd91c0914bfb8471905050c87570405a2c6d7eb146fa2f89058e7cf3a959d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69163305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e509c578d23da614b51f89b21654af9274e10174f6c492b02a3917587a342`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:43:12 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 19:43:17 GMT
ADD file:9450db2cf55b9a98d578379905b5de508c7dff0d20b834c46ea97a5420228a09 in / 
# Tue, 06 Jun 2023 19:43:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:27c1534f45586ad09aba8c625a388bb389e5d9fa9e861a96d8e4a29cd94a612d`  
		Last Modified: Tue, 06 Jun 2023 19:44:06 GMT  
		Size: 69.2 MB (69163305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
