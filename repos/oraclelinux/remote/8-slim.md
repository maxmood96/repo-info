## `oraclelinux:8-slim`

```console
$ docker pull oraclelinux@sha256:f0347e89f8eb3a967e0ea0b94975d5d004e2398f27f980b4b6b2faf5c8b5283b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `oraclelinux:8-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:0e3d7018822b217fe4b69999a151a4f62e505c672181ca064ffc2b265de70506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51293960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063cd2cd55aeb5aac9a54669ffe0a3773897983c6499601690fe6889416351ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7d760ad2fe664c6995a4d9508e389d78b6bdf1b1f154b4a216d0fd3ad9a46bc`  
		Last Modified: Tue, 10 Sep 2024 01:03:41 GMT  
		Size: 51.3 MB (51293960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:0d111105fe13054d5d7a18894e09ce965a7ef5ae55ae1068f4394442d3d47dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231d62137c3050b3aa2d5be3cab7cd8d8894d4693209dd737168c1f9f5bfc929`

```dockerfile
```

-	Layers:
	-	`sha256:11afcada2b4151f48ea990b651fb683ac50ebec84c015166a0670cf8e60acb05`  
		Last Modified: Tue, 10 Sep 2024 01:03:40 GMT  
		Size: 2.1 MB (2081034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd3eb49cb6161ff02d268f94826fd1b8a0b4de255bfe048ed8149d789e115a1`  
		Last Modified: Tue, 10 Sep 2024 01:03:40 GMT  
		Size: 4.8 KB (4847 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:281e74badb2a6eef54525601542635d91f48c52c2e5dd76537bf567b6fa4dcfc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50007867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cffd218c14ad78180f1953833b491bc8dbfdcee331a65347df8e1ead89c367`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:52 GMT
ADD file:6b13879bf605622e279dbcac5c590af19f2ada3a9a83051585288eac41ef5a5b in / 
# Fri, 23 Aug 2024 00:40:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4bb281b07b90a8d48b631141dbbfe6ee3f5d88680eac4b43c59de36db45ca5`  
		Last Modified: Fri, 23 Aug 2024 00:42:25 GMT  
		Size: 50.0 MB (50007867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
