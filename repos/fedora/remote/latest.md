## `fedora:latest`

```console
$ docker pull fedora@sha256:e5c48acb53d1b8738570c9f896777dbc1fafa240ed50be2967f295ff7d0b789d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:6c8b3dea130cfa28babcb4d73450ed64f962e5464ab191bc0539487daf25d533
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64929312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055b2e5ebc940affa3a6e0372b8e7f3c33a5db860173c3328ae36a10cfbe30f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:19 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 14 May 2021 17:20:54 GMT
ADD file:f8b822814d179a7672f993703092ce712247a57be0e2bb31dfbec263041983ff in / 
# Fri, 14 May 2021 17:20:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1495d80d5267d492823f0904735a9bfabb31db73622e0feca7eb53b566acfd1`  
		Last Modified: Fri, 14 May 2021 17:21:53 GMT  
		Size: 64.9 MB (64929312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm variant v7

```console
$ docker pull fedora@sha256:b521cf9c8233fdc78120a56de0ca1d6d46c16b1e172b8fa54446da52d6b33379
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61226800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6ba5f947147fc420a0c9897d66c6eec915dadab99561d6e0705f800b804854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Oct 2020 21:02:51 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:03:11 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 14 May 2021 18:07:17 GMT
ADD file:6bef60588e9fb1a6f4cfb76300ca8924b980d25a8c308245ae9d078590a2fc37 in / 
# Fri, 14 May 2021 18:07:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a367c2737400d51ba4fabcd91f609374934667165f4676c4845f3be7a49c3e57`  
		Last Modified: Fri, 14 May 2021 18:09:32 GMT  
		Size: 61.2 MB (61226800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:547026af245a3430ebc0908b41b36de50251cea4e608a0032422ffd463d67b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64685496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f61b50da8689423cc79f08c69e0ffed97e8fb62f82ebf0e7fa59d92067982b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 01:32:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 01:32:50 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 23 Jul 2021 01:32:55 GMT
ADD file:0284fbd4cfa707f4a01ce87a370bdf56bb66176261262b617c39e48e231ad73d in / 
# Fri, 23 Jul 2021 01:32:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90d9686efbeecc4cbab75e32c01d9b1d7ec0389296ec0a642a6b42e0bccd2282`  
		Last Modified: Fri, 23 Jul 2021 01:34:18 GMT  
		Size: 64.7 MB (64685496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:f9accb359b1cbb461b908c66b63e9f86d622b17759d4f4b733b3e0c1f24b6460
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70685915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3b2004b4b49af07096ea30129744f1c887a1db9e7901f2c39a9629855b8303`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:18:48 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 14 May 2021 17:38:59 GMT
ADD file:80539c5ef570057462dec224a4770a5414b47c917aa2508f90384789b443e9da in / 
# Fri, 14 May 2021 17:39:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e4253e57b8478d2f7787e62a0807b5b04c748fba64de84d75812fddda71b5b6`  
		Last Modified: Fri, 14 May 2021 17:40:45 GMT  
		Size: 70.7 MB (70685915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:856655f3bd7f2f8d9c73107f49de99f1752b3ad7e008b37657c54627972c8936
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62536233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5b4acd0d225dfe7376e57d98f1fb2697129d01c23b78a2b9dff613e652609`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 02:30:59 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Fri, 23 Jul 2021 02:31:05 GMT
ADD file:5011bdb3059844fb9754e811955a1924e9b0310bcaa3d47dcb079b3842f46ffd in / 
# Fri, 23 Jul 2021 02:31:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abfd88677ea830c879e2b85ebf13935b6e06ffd4ee9870da8e7f25bc12250faf`  
		Last Modified: Fri, 23 Jul 2021 02:32:07 GMT  
		Size: 62.5 MB (62536233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
