## `debian:experimental-20260421`

```console
$ docker pull debian@sha256:ee7d121ad7a853d584eac2cb374811eb346795cb9e9beead1224185b579877b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental-20260421` - linux; amd64

```console
$ docker pull debian@sha256:7ae5630163357de51938f5d6a735e471c9d6810e14297b9b7c5ce9138549ee2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48670805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6375c1583f16d2431544b8d0256536288a26c8d91ce8ecbce742a6351bdb2fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:da1b39412060ddb62e7201c79b442133c0f4a701d2cd10e846eb8d608ef00909`  
		Last Modified: Wed, 22 Apr 2026 00:16:57 GMT  
		Size: 48.7 MB (48670584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15e1423f34d994db0e73a59f38741ec659944cdabb4cc55a0fa5965aba4f4e`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:961ec5b96f210b2fc777961708fadec4b5c91cb995a979bb80c6b51ca69782eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6b3d68be75ba3b2a5d80e81410663a0bbf86ad914437088a06d5ba1bc1671d`

```dockerfile
```

-	Layers:
	-	`sha256:678dde4067b053736de5addae94b4aa63b0b1b62d421dbf75662e6749bcba4f4`  
		Last Modified: Wed, 22 Apr 2026 01:15:49 GMT  
		Size: 3.1 MB (3145547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3bcd4a008846e77f3f05f9e0b17248b222a68fcb74103d6f16a0c3a7bb153a`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; arm variant v7

```console
$ docker pull debian@sha256:501256738b563d9b2823e9565dadcbef7a9d89f8557c02eb567151a73b4a465f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45607612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b840847f8e084f4f652465824a04c9ddff3c704aa04cfad43a5e316f85566`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8f4d0f64c416981efdadc732b77011349b8c4e03b427d794bcca746622a8fb45`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 45.6 MB (45607390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43118519c15c3a62870ac931cf476423481d521095ceceeaae1307a0030d2cbf`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:3b912854665956ec914deae6969fa0eff4772d93957ecdf6f7cfd2373e54b0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae77b3bb240d1d74b8d50f2b68eb51e2536097ca84d0bfe878330453e39d9ee6`

```dockerfile
```

-	Layers:
	-	`sha256:64344f8c4a981edf6d314de820dd3eabcbbf0e923a2b8571967622bd736df7ee`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 3.1 MB (3146917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e30426a4804ea6a9b9bc66a2e40af692a1d7cef5f841276b21ead900e430b6f`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:974e034b3c5266700e5352c9be7aebeac2c049c0fb7927b16ddc546b907df38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48711597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8a1e0cd2eae14d55f547c4e5d0dc731f724ef49a969d89248d50fe2b5c4728`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c6b5ac29527c0f10c387962282d51011fba88600d0f076d2a4a2cb9c3f4f7be3`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 48.7 MB (48711377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5b8dcaf4d757a34808321c10de7c40f084c797951535fcabf387a81ae689e5`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:18906823675b5788531fb4e4f6bbe0266f1355382f668420dc43d041e530bc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf70e82e765b6332933f079b583b5d83aa59289149d83ce141c449689a784a`

```dockerfile
```

-	Layers:
	-	`sha256:541b8c537cb88e2550d4f5919daeb9c734a17a048d1f6770b40c3f388a2cce02`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 3.2 MB (3151509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee29a444d86ffb130a3b4f4be8394c9994ee644f2a98b5de4d6bbaaccec8865`  
		Last Modified: Wed, 22 Apr 2026 01:15:52 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260421` - linux; s390x

```console
$ docker pull debian@sha256:5692a10ce1144d16e21d86e85d8e9716f2170175861050d3de27091d014e7da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48411174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fcb394f4fb9c103e1046ae14a0435c9745ab94ad57d1547326a5a698925bbf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:94cc507370142df8a6a6c11401d1d18650ae32fff6ae2bcb0d4e4840a1e93548`  
		Last Modified: Wed, 22 Apr 2026 00:17:14 GMT  
		Size: 48.4 MB (48410954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b2264f2100691a855189e3fae7b28d33acf32d60d1813fb8538deb5c6b4bd7`  
		Last Modified: Wed, 22 Apr 2026 01:15:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260421` - unknown; unknown

```console
$ docker pull debian@sha256:9d8e1b58da98f61fa329f0a29988b13e83eb8a22cc8891093607029569ab2321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bac0f3b56f3e0dcbb376d753b34241dcc9c6e29b938460de590cc3a010a82c`

```dockerfile
```

-	Layers:
	-	`sha256:b82725623ddbfb1cabb3ce0e671e951c5870626c8493cc86977a4aafb5329c26`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 3.1 MB (3146998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0ff32e27939189e699bd7a8c9881160f1a13ba76272de5c734056c06c3282f`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
