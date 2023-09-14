## `fedora:latest`

```console
$ docker pull fedora@sha256:6fc00f83a1b6526b1c6562e30f552d109ba8e269259c6742a26efab1b7aef59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:77483e31e379165486cb8c89eaef7b9b0a169b47885fefdedc252fdeeb31d4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68534858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621310b5b7d8188469265c9e0ce793ee72128e5e5ff5cb935a527b73873e4808`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 14 Sep 2023 19:19:57 GMT
ADD file:618996341feb53c758e52c175fb0b6da9c48dafde92aedec2a244d29bc7c76ab in / 
# Thu, 14 Sep 2023 19:19:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:feef24b52eb3530f7b1e92d98f79a346fa12d50859651342443d7d3bf2a6f2c5`  
		Last Modified: Thu, 14 Sep 2023 19:21:00 GMT  
		Size: 68.5 MB (68534858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:b8c5ed7a6028f79cf2b08dcdee05aa10fdc1310571878614aa0a733844d260a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9b2be3019115d2460cf37beef528afea6c55004bc7f63929f5326f0e363d5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 14 Sep 2023 18:39:58 GMT
ADD file:648735b60656251081bcaa2d69d2d39572af68c21a80f866632f5156c56b12e7 in / 
# Thu, 14 Sep 2023 18:39:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f576322729671deb6b27aab6de05c8f4233c7188c25f29aac9ec17b81c5c350a`  
		Last Modified: Thu, 14 Sep 2023 18:40:50 GMT  
		Size: 67.3 MB (67298615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:2ed9e82941fd29efc85ee953873628d74a610c1884fa439a8309b69d7ce3a0bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75667523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d6a326a25bb123a12d5626d0ad8584de724711b2fbf5b0d71e1e924039e515`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 14 Sep 2023 19:17:20 GMT
ADD file:b0c14a6bfbe2ec20cc1aef172ffd67ea46ce5b1092850c32c70ebe8d67ad2f0d in / 
# Thu, 14 Sep 2023 19:17:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:441978dc49db258e95472d45ef99c85f007aa7a2f8629865ed8ef1df448eb429`  
		Last Modified: Thu, 14 Sep 2023 19:19:12 GMT  
		Size: 75.7 MB (75667523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:ecfceff1eccb1c43664c82c0bd1e8336c72b2907496b9ed07c2740e704e0e588
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69223669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013c2372e10650f842608a38a3d4835c4f5549ffe71a899c4524509e37c3ea1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 14 Sep 2023 18:43:00 GMT
ADD file:0aceab038e66e33c744ad2f258310bbe0b7fa840793ea52af0466a34db86d26b in / 
# Thu, 14 Sep 2023 18:43:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:497f9e8c682f9eefdf60f138039e3fb65833d06992a166038e8adebde19b0bb9`  
		Last Modified: Thu, 14 Sep 2023 18:44:20 GMT  
		Size: 69.2 MB (69223669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
