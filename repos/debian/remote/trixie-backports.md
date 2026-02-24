## `debian:trixie-backports`

```console
$ docker pull debian@sha256:0c1190bbfee5b2a21cf8e260c631f14daabda14f9bb187b6b3fba8196886e6b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:83a5fc1075a4d17070b84309e9d3c9766aa7d3af7849bb3edb2a987833ea9466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cbfc00317db88ae15e4244a7c9b023138972638e606e0e5795b84d61b19b6d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:52:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849f41e9593390705dc2eb3185ffb6068b59837f48ef75cf68d37f8e1a671d5b`  
		Last Modified: Tue, 24 Feb 2026 18:52:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:97d82514067469edfc9b0bc984702cc6624d522c8cc4c49fbf29425114012fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182ee1368a33f0ac73ffb7ec885733057044df501b3e47ae32c545526d1c884d`

```dockerfile
```

-	Layers:
	-	`sha256:c2d9e942c070567d5c5724b348efeba6ec7f64d71ebec3672bf926a527f3a125`  
		Last Modified: Tue, 24 Feb 2026 18:52:06 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c47e0e5ae2a35b3ab31a9578c92a49385403e157cb38504084a67ffdebd5b9c`  
		Last Modified: Tue, 24 Feb 2026 18:52:06 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:13808b7bad795419b99da59dd88201fe0bcde72ca1bc961baf7e3d8bf88a94bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47454385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fa46119910c999576cae2b12f95bacd294fd33f332129797d1479ad35af4dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:53:51 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6c0530a0840df8a05679f77d095cbed0674c87160dab8f0e65ed5257ed4b0ca9`  
		Last Modified: Tue, 24 Feb 2026 18:42:14 GMT  
		Size: 47.5 MB (47454162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae77cde429bb9f923646f8bc05360969aa011a7a3360296d571a2c834cd1dda6`  
		Last Modified: Tue, 24 Feb 2026 18:53:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7175cf59ececf4b3046f25b5dc2de6496e38ccfd3a58439423bb6577845052ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f5eebfd02bd6346e5212393dfe992b497e1d792b9c872b4ed899096673f3b0`

```dockerfile
```

-	Layers:
	-	`sha256:8f09c2d0da74a11daa8df468de6e4a2badc96eb15f2c057468481e90c5d59ddd`  
		Last Modified: Tue, 24 Feb 2026 18:53:57 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18faa033098c085a4d725a91cf4d9346801add6c7212455fe4bb3026aa4dd09`  
		Last Modified: Tue, 24 Feb 2026 18:53:57 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:21060bd15963394c4726e57046b543cc4d950bebc423910edea4ffbb506a7c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45725310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8fb4bf61ffc66cc683c7419e1a8b81071d028671a2f76c6e2feeaba93455f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:56:35 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a621db956c82b7a96409d8b873ba22dcae4bf1b620127625d24e1f0849578f1`  
		Last Modified: Tue, 24 Feb 2026 18:56:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a5acd7b4bacc00d1e74da71b871204414b5e8b8070ea323da4d7032e5f5bc168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984b09735d8cb1dcb2e05b0328bc509dfd2bad6590b399650344a44bbcb82de8`

```dockerfile
```

-	Layers:
	-	`sha256:6750784fda76b542790fd4acb9e02bd1582dfb7df58bd7427e89823910635f3f`  
		Last Modified: Tue, 24 Feb 2026 18:56:42 GMT  
		Size: 3.2 MB (3172251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450b590c1f616ec4d1a54d542d445307e8cbdfa740e13b063556e5408f514072`  
		Last Modified: Tue, 24 Feb 2026 18:56:41 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:637cb21501b4b885939fda88d61be81750f073508612a5a62cf065c594929660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49652391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8583ad2a92288c3d3d54848f1bb2c611281ca836f77a3284db44cd1b0a627`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:57:22 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557242bb4f7b1ff5c5e944d075a0606174e718f051632859da7de3287a8ceec2`  
		Last Modified: Tue, 24 Feb 2026 18:57:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ae4ed245b22736b2c32d01752e3cb5c7d12de25c4ade7e8d4d08efacb26132a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8c87e083a59c184b04172204765070ff72e83a4a145835243a4afc9500f77b`

```dockerfile
```

-	Layers:
	-	`sha256:43d14ccb5eca1b1dc5b1615e9f1515f6e201d55481fef5e91cb35917b8982a97`  
		Last Modified: Tue, 24 Feb 2026 18:57:29 GMT  
		Size: 3.2 MB (3172358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804c63ee8982c173a3708c8219ffa729e76abec64b17ab10e2d6f7d81c115a0`  
		Last Modified: Tue, 24 Feb 2026 18:57:29 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:f9f478d3ffb3d9fffcdac4678083d5985f59762c8163025f6c1fe3f4a6091a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50805495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7382606ac290193f48b975b077c32d4d88799e75b38fc888e58cceb2b346ac7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:54:11 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9462fe3c4fa100cdc1900f6ef64512f476043d1e415ae9ea0c4690624da8530`  
		Last Modified: Tue, 24 Feb 2026 18:54:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0239daaa16651c972db16a82eb4af34abc0414e5e4136c457d6b3da5985360cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8c321b8f7017ecfc029fa64bc693adf0be1a41788908b37694d61d7945e30f`

```dockerfile
```

-	Layers:
	-	`sha256:dba2ecfd6bad75e4c17c67516c5e95814f3643a35e86531cb1f250742ee36c7b`  
		Last Modified: Tue, 24 Feb 2026 18:54:17 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9b341e11fd26ca14f527fc9e8eb56df2b066b93660ebe955a35cd8c4556e057`  
		Last Modified: Tue, 24 Feb 2026 18:54:16 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ea870eb01457e9d1a08e8411c049293f08d6bb854ac3860352fe17f8af46a49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53112484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbf81fbab4a7b9ed5e440c7eee087fae65463f052a611cbf65891e5cddf4ef1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:54:41 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66be9ce87380f8681e265d318f3bd659204e61a444e57813970e6d80e65060ae`  
		Last Modified: Tue, 24 Feb 2026 18:54:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:76a6fe883cfc007c8ded336589433939b3ad417d8a3e2ef031118413b827b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ca8d2d7c82932df5d316dc6166e75ec895cf9775d7842cb548e38012b68d26`

```dockerfile
```

-	Layers:
	-	`sha256:9112e4e086b726127368cab6f58585e924d5ed24876ccaa89c0060451625dcb5`  
		Last Modified: Tue, 24 Feb 2026 18:54:55 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa852ad2510fee642153a73cb7386962308c3fdfb75e47097e5fc401ebcd6cd`  
		Last Modified: Tue, 24 Feb 2026 18:54:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:ea793a8f41f74cb1fddedb44bdf8b15710fb035cf745559d60c4d3a13532e543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47776988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd68144192e91784cc62e02f6243b291a7892f55ede849b5530d6d5ff643dc9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:24 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea4f72f51d5d16106d3f62d5cea22a458da29a1fb10b956b9924b08f45f92b6`  
		Last Modified: Tue, 03 Feb 2026 09:05:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6bb9aea7ad61edf4bc90d3d03cee22bd959c785fa948b27b1bd5449287270b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a1bb7b433eabd4ddf87407862e8826280a9e2fac40d94193d85fddb5e63d88`

```dockerfile
```

-	Layers:
	-	`sha256:04769e32b0bff31fe5d200ba55690592543f62782bd20f246641c1400a4cc4c8`  
		Last Modified: Tue, 03 Feb 2026 09:05:19 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1099b8b5db41d5fb21be52b3443f878dc6fdc8e33d6a7c0b6f30077b250bf72`  
		Last Modified: Tue, 03 Feb 2026 09:05:19 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:cea61672290adbaf4c021bd360e8d7c3de591bcfbbc968cbfef1defcd940e2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49354758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dfaf2e0f7ed662471c17ff26668562b5f454ddde85990380f16974e972d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:53:56 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf23d0ccd949ff2e2ab257ee419becc59b1eec36ad12255ac822a2d57bd1b169`  
		Last Modified: Tue, 24 Feb 2026 18:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:304e9cf25f419e340134ed3cef9f6ecb02ff047bed5e9479be9a1550ffeb6951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa94f665cf4525d2099f0a84bf4124ae193b1e503511576a414f850d5f8ff0`

```dockerfile
```

-	Layers:
	-	`sha256:b52bb8282ace32ad2016201541a2bf1ee690ddf2f4b73d02ef3ce1b836d554a9`  
		Last Modified: Tue, 24 Feb 2026 18:54:15 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be35738c882240717ae622e29dd139afb803b69290102eefe9df5aa02cc1519`  
		Last Modified: Tue, 24 Feb 2026 18:54:15 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
