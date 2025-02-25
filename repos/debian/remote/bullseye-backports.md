## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:214280cce928aba3b983888877617d12de88286f39a51ce856560f88a3b0f032
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
$ docker pull debian@sha256:5b332940b2314b669284353c9a1278539821a96745f67771cd30281d147d623f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53741629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a852f1c75534fc5895c280cc72c14533d4ca5cb5948d54af78a517e283617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0627cbaabe0dac49ee89df59c0bed11a370708c2fa7caa849aeaa5487a4218a`  
		Last Modified: Tue, 25 Feb 2025 02:11:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b0e605f4c95a2b8a573c461e84939493c3cd21505c4f0fcdb74a3aaef3108db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f5a61c1008cdfc2a8c87a67008964743a734320898986017f9b823cdd75a4b`

```dockerfile
```

-	Layers:
	-	`sha256:0e19ca01ec671574b7bd77484c33cefa6b97467e522d2f6481519747280114d2`  
		Last Modified: Tue, 25 Feb 2025 02:11:28 GMT  
		Size: 3.9 MB (3917516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3d629b8cbb32859478502c88f416a761c69790a02fd3c4d0cff2da81d33798`  
		Last Modified: Tue, 25 Feb 2025 02:11:28 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cd292d330589c0636bb88ec3cba67823bf33d9435e8f8c85e53ea42a2f8d286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49026958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3a367008d7ee2a7642fbe122702955d8091197ebde623b26c55834cf5c7b26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0a105bcb5f89660fbb37b5154f974ceb69f1adb2d5fab6a09d5671b6de670d`  
		Last Modified: Tue, 25 Feb 2025 02:15:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8beb0cea05ddd22a080d749c278b5567945d5923541a161fe0cff7e687c99212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561b2831963bd295bf65663850e3630941a5908d68766fce5e8f6fb332971d61`

```dockerfile
```

-	Layers:
	-	`sha256:985c59cdffec1712e862a31258c1cc49a81e4a1af332e7db7216c75c6ca4734c`  
		Last Modified: Tue, 25 Feb 2025 02:15:43 GMT  
		Size: 3.9 MB (3919078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890313f7e92ac9dfd410be1fd6f0286b50abe8ce55916af368e6ae04ee73e04a`  
		Last Modified: Tue, 25 Feb 2025 02:15:43 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c9dd5a8d568b14aabb28e876d9beb741cf6e38e70fa9fa6dbbbfc957c94d16fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52248868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511e83cd37e6c7a3afed234fb2036a372e6291771afe8b67a233a6440c753a84`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c62abb73c5aadbe4620ab108df0dd2ae3cb69e71725c3a1886af930b7c70a5e`  
		Last Modified: Tue, 25 Feb 2025 02:16:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1d9e6dc644d47ba4dc4961b25a08b044e4eb8d8382486cbd4fb213b753a0046a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83eff8c97eb03735628c8fd0f6368f451ccca326e318c2e0f2106e7787caa270`

```dockerfile
```

-	Layers:
	-	`sha256:83a83492a309449621b6e7c970e501c93c9a316b6b766b7a1c09ef394eb37dea`  
		Last Modified: Tue, 25 Feb 2025 02:16:40 GMT  
		Size: 3.9 MB (3917096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19cfcd2664b3979adda47974e7293a58a6392927bc7a7c69e43b6861cae2a4b3`  
		Last Modified: Tue, 25 Feb 2025 02:16:39 GMT  
		Size: 5.9 KB (5914 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:d7931bdb46f85b10d3124196019c8977e0b5e9452f4d3bb029e2471da4a2af3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54679089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34c87d51c1c72e364007c7bdf62e9f42c36d4af4f96df9178261b3cfedb7f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4b7ce1a99e2125d01e65c7f36fa44ae061021bf32484380434c6630508365`  
		Last Modified: Tue, 25 Feb 2025 02:11:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4d2e515038216b4307bde2bb78f40c3f63c630ddbd08ef54aa66191ff47b1150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82487eb00f01b372c4bccc5f13a406de898c0b8a71e94b0a517a15f84f38dc43`

```dockerfile
```

-	Layers:
	-	`sha256:2f1a96ebd6025c4403ce91f34e899beac24cb678c480da86374e68121628d8ed`  
		Last Modified: Tue, 25 Feb 2025 02:11:17 GMT  
		Size: 3.9 MB (3914023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf05e289c7dae7ea5ba310c7a3f0622cad8dd334a2bd862fe03576d82a71994`  
		Last Modified: Tue, 25 Feb 2025 02:11:17 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
