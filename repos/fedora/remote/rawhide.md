## `fedora:rawhide`

```console
$ docker pull fedora@sha256:fc37c8d50964f07e209d3c1025df58cce03d5c9919db795589924bc4b16cf8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:c230f8f601bffc2166d5923ac5dd83c7e331c3925a85ada4b7a5fe59146b3b69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64774359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28f3a8467eead3f9295637c7ec0539d1032e4de15b19a94d418c6f96b49ef05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:32 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Thu, 01 Apr 2021 18:00:38 GMT
ADD file:6cbadecbb078f15f0df3cf49587b2b26c0a1c6b21710b54ccd09f48be0362c97 in / 
# Thu, 01 Apr 2021 18:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de972ee947b83b0929bc384a239aa4f8d69ef801156dd1bd0ed2578a6a21ed14`  
		Last Modified: Thu, 18 Feb 2021 22:24:57 GMT  
		Size: 64.8 MB (64774359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:53505127f60d80b678137249786b54958a8b3637c44aa3bdd75302583a5dc59c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64754994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623a234e2fce9714c1781bc2469edd4599fd3415147e35b4b56873e5aa1e7863`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 25 Jan 2021 23:41:07 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Thu, 18 Feb 2021 22:53:14 GMT
ADD file:8604e55c9ded0b9d73ecbf93eb87488efc0550fb819a560a5bab97cfe496f30e in / 
# Thu, 18 Feb 2021 22:53:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8437404d345914967894d0a9b568d4c63fd2221346d1f0313ce6f21649c2bdd8`  
		Last Modified: Thu, 18 Feb 2021 22:55:02 GMT  
		Size: 64.8 MB (64754994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
