## `debian:trixie-backports`

```console
$ docker pull debian@sha256:0c840f6f38ee0a0ab8c00e73cccd2f9bd0295800df07c6d6fa8eefc8046b7c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:3674af50cda5c838675e5e9e97bc3e7a3870f8824553c4720e5cdff2542bc5c4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53153173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b252f52c2117c126ae6bb9991b38571f41697444b058c0cc37fd00d01301c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:44 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a928115156124e1003c72c6da74c08bc78500c0df71319b6e33b224280a9e4`  
		Last Modified: Wed, 04 Sep 2024 22:37:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d8c1bf06082b31f1380fbc60ee5dd0d858b73140bf310900d9b52e398e2aa0c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50107303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd64f0d206f2f20fdf33d70c7555be4a10cc458957b6e3e96f2c3156f725ec92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:50:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c0158545cfe41fa0d7399535951c162d3bdcec0ee0963cfbbc546dbcbe1514`  
		Last Modified: Wed, 04 Sep 2024 21:54:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:93d2b780b11329e21982f5527da272c7ee8495757fc7d0d1d487901429f0e110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47600599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2630fb569bf5d0c71b8bade2b0105a1cd14f3a67c84a7444a7c417b77b326295`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:00:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdca1c41ebee8045460f54596a0070ddaf60cd6319d5d4962425025e2a5919d0`  
		Last Modified: Wed, 04 Sep 2024 22:05:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:56b5e7b1a26cf95e2625d302baffff068f3901d1f589d33f95a3e24102866ab3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53594563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237620039e3ee4aae0fec74a430db3b8e2e627d1e9a2bede1b5cab770403f303`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3cb60707e31637c943150854ad9be94c696f2fa1ba4b310f10879bb6a1ca0`  
		Last Modified: Wed, 04 Sep 2024 21:45:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:f54b3ce576d4d6c2dd2ca8d444a2fef80dd2055c85eccdbcaae8b4f326c52b5e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54024509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db97281d74ed5e302da8e027461bec0ce00f8f17e99fc4d3fbd107301540fe72`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:46:33 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a27d699688e09241c00952262bf780922ca881e0504f610e69d2dd50269fbc`  
		Last Modified: Wed, 04 Sep 2024 22:51:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:44f8fa1be6b6562bece6039227b11b9c2bfeaec8fc9481622f4f8a7f7bb8dd88
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52218677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdb32bc18942b9c10999f0cdb688bba28af6355370f4029dfb28cdb60fa978f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:20:27 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb967ff4a80a637116cfa40f28ad8e83c790a1256c72fec14328034d3d4f45b`  
		Last Modified: Wed, 04 Sep 2024 22:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:20a68c381cd7a857767ebe6e68f46465285ef632e0ca567bdb43d5f211a00c4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57078008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af949dd86ac5754efb3c58d959bfaab398860778c9d49faebb090759b2809f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:19 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e356975183d4c46a0239b8113369d5e06569d957f994cb6f25418eb1342090f2`  
		Last Modified: Wed, 04 Sep 2024 22:33:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:96aad8116036d4d010e4f2bc278ad248e89c7656c58e10752ed50c12bd55ea8b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51475751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42d8ce856fd234709ff99aaa64a19e9aae2f6e872f552ddc579f496fd9237e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:03 GMT
ADD file:3536049154c2250abe969642d7b35b085e3d25447b8953cc1e072b690a306aa1 in / 
# Wed, 04 Sep 2024 22:28:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:28:17 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:38a3e7af214e5e0705f0ceebc8bef13cf31414ef0eb3f3ad8a05574549c77869`  
		Last Modified: Wed, 04 Sep 2024 22:33:47 GMT  
		Size: 51.5 MB (51475526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe853d9c0fbb58c46d314446eeb6458612c8bdf15d74756dcf70dfbbc608cd3`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:972f65a1be5b24b6fee02d1f8fde22686f5ab954daf14fc8733d95acf62a4b5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52746678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc400e03cd0bb6be74d0cd994fd96c66e468b3ad1a7c289165048d96ef1a72a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:45:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcec886a2ce18dd72e992d37233999cfbbb785926023daecb929517c3399a9f`  
		Last Modified: Wed, 04 Sep 2024 21:49:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
