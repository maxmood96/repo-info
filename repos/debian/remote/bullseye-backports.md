## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:963fc9f919f5bd7bb5ed6f9d9c844eb3edfec0178769fe0bce66e4d511f60a86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:7ca61305491e2060966f9bd6418bc0beac7e9e42b95fab5948008b964398e537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53748755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6441bded14ac1ce23d3fc7db54ecda8b49195c8db9ec2c3c2f9cc9a5241b9134`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112bc87b324a55ee682bf2a1f38e24d1ae1757aa6d871b93762f95f39593a7f`  
		Last Modified: Tue, 08 Apr 2025 01:11:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:87f4e74f9828faf0bde44cc7e881763fc1919dae9858253e185953346b2bf504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca7485b0fd031ce4d38e3b7f0b09f24079fcb117cda48922b79e0e01cc89b37`

```dockerfile
```

-	Layers:
	-	`sha256:697f1c82323af146c4ab1c9ecb2038818c284e18c913a6644ae7ecf777d8e309`  
		Last Modified: Tue, 08 Apr 2025 01:11:25 GMT  
		Size: 3.9 MB (3919430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c76746294a4c83ab42a52f3c4c678a78b112bed781894e37a8a85d36ab6791`  
		Last Modified: Tue, 08 Apr 2025 01:11:24 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7f61b474761f3395c7d7f60321a4af869066e6abee2e59ea682d4dd14b0f5010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49031674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a497cca6142a97bff710cb911807a4b6ee709dc8afbec0fdca9bc4070e43778`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291adcb388e35ed77c48f69232931c9fef7266194621b309f0d895256aa9a109`  
		Last Modified: Tue, 08 Apr 2025 01:11:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b75df0e6e27d8810bef567d31321b63d2cb12e3367e336cb9c15fc74a5635203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ac0e8e1b4bcede6e11035c5ec6e65eaf8aaeb12f749998a11c0e8fc7f74c5b`

```dockerfile
```

-	Layers:
	-	`sha256:13c1a569d045e847c185b3e0792eb59585723ea8bcdca569cd72778ecdfd29c0`  
		Last Modified: Tue, 08 Apr 2025 01:11:53 GMT  
		Size: 3.9 MB (3920992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07e1b8c8a6027d87498ebf802e6ae5715c35e00cf1057bc827ad23ae30308030`  
		Last Modified: Tue, 08 Apr 2025 01:11:53 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5f0c0178c4f02553b1158304f6d5c8bdff2ac9cc9c52fc48ac074cba25e56d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52254448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b15e8ce18abf10fa06409ff228a818b77ffb350eb7c57f10a911c46110ee09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bee07e479a335a79f8febd06951ea1a7d04d14e5a8703dc5bdbba78403620e`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d5646ac1b1e0d9249f7f61c5fb7f259d0a30c576ebc7d4432323368355753464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a33ab204bf2a99b5e2b59d32cc2341deb14ab6f602bbecf7c6a55758619b384`

```dockerfile
```

-	Layers:
	-	`sha256:ae4bf9271f2ca065016a016f51314b8a02f70ae733c795e4a5283cf9f91f482b`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 3.9 MB (3919010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d79637b94c85f5fe1581d0ab271b4f066906725656cc4752d70e8dee2f03c19`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:262fadcca55f1328b3b4a99a015c8cb1e8818457f49a3d484361822fbbebf1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54684691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804c8ddbb543c512252d485db0941dc6c16244f25389d20376d328acff32bc8c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1776686301baf0062b6cc31e8299f45a242b280a73c8396d937b534f8088fb`  
		Last Modified: Tue, 08 Apr 2025 01:11:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:891b8accd1a14bce0895110cccc0dae69eba6e3baad52823d3c669f62a6d1575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f394835455b05f67bd4e4818e9ab21f5f96abb995b9d0af57a0d83685e54edd`

```dockerfile
```

-	Layers:
	-	`sha256:81b2e9c03606d7c6b4c84c2668e4784549c1df7b7c145be5b5ee215579d3a266`  
		Last Modified: Tue, 08 Apr 2025 01:11:57 GMT  
		Size: 3.9 MB (3915937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f4688b4940c9fd7b71d7e9d6d4b70f0a85a2f477e390ecaf142850f48fb3cd`  
		Last Modified: Tue, 08 Apr 2025 01:11:56 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
