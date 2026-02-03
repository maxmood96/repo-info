## `debian:experimental-20260202`

```console
$ docker pull debian@sha256:1275f0dc55a9750609bf1ec16cdb40e6821d9b6b2c4f8950f4e82d9dd31bac5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental-20260202` - linux; amd64

```console
$ docker pull debian@sha256:cc357e63a86058b3123062730a80ff17caa0a7e3be0d9e9bcf18ed5fb70f92ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48654927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7d9a4b8b4e3b284d67f844b7e38bcf18465f8c1f5d24207be2e6ff53fe34f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5d328c471922b9c24eec6fe86b088870e4bf7f601f2dd72d0bf170cf0a5e1ede`  
		Last Modified: Tue, 03 Feb 2026 01:15:32 GMT  
		Size: 48.7 MB (48654704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f2c2d49322d97bac078c70b67b5a2e1886c97e3212e01960608ba15cd5954d`  
		Last Modified: Tue, 03 Feb 2026 02:15:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260202` - unknown; unknown

```console
$ docker pull debian@sha256:ef7c31d739e7cbdfc939972bfc888bd8e9efa4fdd06387ced1477fe2d136de93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7509e513cbfcc20e134f73b9a71a7286e07c39e5b6d6304433fd80e8e692d485`

```dockerfile
```

-	Layers:
	-	`sha256:e0a81bc5bfcc06809cde997416831b7d3d0f7664fb263bfa664a68b09bdc9e5a`  
		Last Modified: Tue, 03 Feb 2026 02:15:38 GMT  
		Size: 3.2 MB (3150471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd4797138a4802a5a449ea0fac1c5327a33954d4aaf6039e45dfb7a818467d0`  
		Last Modified: Tue, 03 Feb 2026 02:15:38 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260202` - linux; ppc64le

```console
$ docker pull debian@sha256:b7e6ab7ae285ec084cd3696d38c6e74d2e8fb1232abe29de6fcb3dc59493025d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53584743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf987cefe99aae1f0a546ec45880105748ae5452e97dc52ff1c7041bc338c04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:ac9478d372ab9900a4f99ed9d427a96a3de37a06833f433b4f9dcbb81db19679`  
		Last Modified: Tue, 03 Feb 2026 01:17:10 GMT  
		Size: 53.6 MB (53584521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e425367957ebad6dc87d076146bdf278a2c029badf97a481bcb3c3a6a8648b47`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260202` - unknown; unknown

```console
$ docker pull debian@sha256:ebc54fc5a65c96bdad416d239f4e8ac521800f61043a79fc03916b347f676ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df96465c72bd1c218dcc5bbad07c562447f47ac8eac07452ac75e690114b0a0f`

```dockerfile
```

-	Layers:
	-	`sha256:c1d136a22d6bcdcd763be53ef731dc7c158f0ee039fc719ef00dbe2a8ecbdd40`  
		Last Modified: Tue, 03 Feb 2026 02:16:10 GMT  
		Size: 3.2 MB (3153998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0abdad9353de66dd1cf4ee387c162240ed1d188703176c4742d1d96f7d9b6945`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260202` - linux; s390x

```console
$ docker pull debian@sha256:3b87610a949a9fa3a9dc85956d52405911a297d3b6efd31836058c63f4377603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48421418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f825f4c32ba5850e7ad1c61925bb666b84144273571e6e184d148f84b6a8f56a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8a73935faa923da850aad16997bdc7c93e6f2998a9394fd1cac6755ff322159d`  
		Last Modified: Tue, 03 Feb 2026 01:14:18 GMT  
		Size: 48.4 MB (48421196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce13534a47666f9ad075307a5bb32e126837bf5367c3afdc149d535e2991f308`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260202` - unknown; unknown

```console
$ docker pull debian@sha256:26be35bdbc8de41658a128a71b52ba6fe1ecb1d7d6061198a26ae47d1ed172ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065b819aa492a473f6425e7454f90665320a4be8166a0078fb5fa58766dea00f`

```dockerfile
```

-	Layers:
	-	`sha256:3fc7095c7de702422b40901b2f243060cf67ed77de5f8c7b8b7dedd2772c7441`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 3.2 MB (3151920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da51458d1cdd98e6acb26ae34259b8be9dbe6f12f10d28f6641b61e96182c6f`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
