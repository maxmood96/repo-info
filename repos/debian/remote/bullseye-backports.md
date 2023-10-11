## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:5a61c279d936ea0c9f446a903475d14df185f37118b41d719e864e9d1e38d6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:97238abb6dca80acb06033eaf23b6cc203088f4a0ff050911125936685fd7595
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55058253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75d5046383dbcdf8795a6a1015fe6a011958216df4cb2fc892511b2d737df8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:35:05 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54953a549560f080ebcd31c86088e4a4f1eeb8ed3c5fb5aaa4b46059492c40f`  
		Last Modified: Wed, 11 Oct 2023 18:40:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:17b0f7da7b9ba794f0f555a3ac21ff2a8c4c1bde8eeb32db6353598831a9fbb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52563324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39011a144cb1eb41668ad5a709c3b820b3388336ab2a108f7527d7684a46aed1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:37:51 GMT
ADD file:dd011733a11e4681328b2d45bbfc478e1dab88a95554fe817e238ef27b1865c2 in / 
# Wed, 11 Oct 2023 17:37:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:37:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d310e2405531cf391481a06c9f4d0fc75165ad8e3025e4035c6be5245b6cc754`  
		Last Modified: Wed, 11 Oct 2023 17:41:07 GMT  
		Size: 52.6 MB (52563098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2909d0a72fc0c081b334097a7d29d215a18848f53621c9843396f284507b587`  
		Last Modified: Wed, 11 Oct 2023 17:41:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5def4c264e6d6e57d4e8c45965226c9d942da75f87f07a2b63386e80bf9d0e84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbc03aca5220e21e3b5d4a2dcc4a732f8565c94de4e302e65aaa1d4070637f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:19 GMT
ADD file:684f3634c6b747a4caad8f9f820cc02b53a2122591fe215935c5497ec234c3ad in / 
# Wed, 11 Oct 2023 17:42:20 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:23 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:33d0c7672db93e653471872c639cd6129ec25c168942e15a008c4920cafe62d7`  
		Last Modified: Wed, 11 Oct 2023 17:46:42 GMT  
		Size: 50.2 MB (50215704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb60d233fc438b39d82595d19e442d497273eecacaf5c50cb0ace0929be8156`  
		Last Modified: Wed, 11 Oct 2023 17:46:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f5e5ea9ffdc2ce64b74c68123e863e5875904c5350647e36cb23d6567c1793d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e5eef923d4e10133e7c75d8aa23924cdbc778f2f95cc82a648cbe91f50d8dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:25:01 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1e95f6fdf14c244cc7fbd0344ff1b2d3cc1e8b78ce56885d361a1333b436e8`  
		Last Modified: Wed, 11 Oct 2023 18:28:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:124bfb28783bea14b17dbbe0542f5bbbffdde9fd1e326da7b333a469c2e71b51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58209120a8aec2e063045eab6d5e1cc48c0343703a93e11dba0aada495f93743`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:40:52 GMT
ADD file:a3c1e94bb116d940a614a5275c69bacbac46e00da2070b5c7a561e64b975acc6 in / 
# Wed, 11 Oct 2023 17:40:53 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:40:56 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:081c634ff059d5636b4292d84d0b49429030b3dca70ca56828543b295adb9d47`  
		Last Modified: Wed, 11 Oct 2023 17:45:55 GMT  
		Size: 56.0 MB (56046358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccf9b5d57e39e095427103e619e59a656597c1614c6777a6367e4cafca67705`  
		Last Modified: Wed, 11 Oct 2023 17:46:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3c57aabe7f08a1c6705c540ebe63243ee761247d5b7883803c085e3c3b848796
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ab58d21bca0ff8c7e24cc4fec98b5af6cfdd5e912a11d2c2b3305ebb87dfc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:06 GMT
ADD file:c4be7fca661f2a8181ee1e05fda057c18a2d7c1ae0e08ab63b2c5567ef9cc0a7 in / 
# Wed, 11 Oct 2023 17:50:12 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:50:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d237f50a9f05adf465246bef37e194e1d7a226224c7f90ae7b55925c5b509d15`  
		Last Modified: Wed, 11 Oct 2023 18:01:27 GMT  
		Size: 53.3 MB (53289043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0c8776a8149e5c5980d9f057f171a6d6a5c7f95a6ed33f3bdacdbc74aa643`  
		Last Modified: Wed, 11 Oct 2023 18:01:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d8812aee9c2e736d95754db3cd44ede3e72370da17054a98592aef27b8eee943
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8555468b068b06459a4fe7136b0cc60c3ffa57f1aef7e04919a29eaac7abea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:35 GMT
ADD file:d59326770edede2ba1d2005697bf41540a3d76a4bae883b91fede9b68018630c in / 
# Wed, 11 Oct 2023 17:44:38 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:44:42 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6613fa9f09034273d2b35a47386f8d53c77953a73e561b9f189ffa43ea17bd54`  
		Last Modified: Wed, 11 Oct 2023 17:50:25 GMT  
		Size: 58.9 MB (58929717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0582c32842e672c2015f29bbdd920d5f2d427882016ca0914be6e315e2c18d`  
		Last Modified: Wed, 11 Oct 2023 17:50:39 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:e8832581bbe88982358ee27884d5290578c08142ad937c3354656d3aa23190f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71e21840264e8579c8b2756de132c16edead5d358a83e920a84fb6b4fc8ebd2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:40 GMT
ADD file:bb3ee20a7ddf364b23163c517132146872491e85ef2f1465bf7fd2ed33f94827 in / 
# Wed, 11 Oct 2023 17:50:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:50:50 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e651436ffb848f56da62cd2c80f206a288b94da8113c4c23a7e5502fb597ce23`  
		Last Modified: Wed, 11 Oct 2023 17:56:38 GMT  
		Size: 53.3 MB (53296378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e4400b100e9bcff0bda6c130ec1906f16f222aa28025bc2c3c349534dea19a`  
		Last Modified: Wed, 11 Oct 2023 17:57:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
