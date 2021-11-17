## `debian:rc-buggy`

```console
$ docker pull debian@sha256:6e91ff496972650d761b068bc4d5d340a7d2e1c4de2b877fd97d4b90c2bd6c2b
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:297cc93165d2ca676dc67f86c1190c4ddc3a53bd71c622e1a6b27b9efd2c2362
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55758317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd5266ad852a3b4e61c0d107a89fe0e283b14dab1ee3d2823a422ccf3ac302e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:50 GMT
ADD file:1f62518cec36eb3320e38344c0d36779557214cfce8bc32eda000183a34a0ffa in / 
# Wed, 17 Nov 2021 02:21:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:23:22 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0fef5443775fe054990b02e8f72c4c5bc7792c6a5bf6ef8df110873a81676a87`  
		Last Modified: Wed, 17 Nov 2021 02:28:03 GMT  
		Size: 55.8 MB (55758091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a959b47f81cc0d14fbb210c9fc123b9c76b0123bc4bf18c4c1f0695198ea50ea`  
		Last Modified: Wed, 17 Nov 2021 02:31:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:7b6405b207f9d0e7cc57586feebe2ca61efcaf79ab2cc70db866170365157b9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ba8704ecfff8b7fac421cf93e23ee0ceaba7e4348758051819d0ea539030c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:53:53 GMT
ADD file:2918872df07d47b9a7862abf3b22f39600ab45587fcd02466bdefa775a3fc2dd in / 
# Tue, 12 Oct 2021 00:53:54 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:58:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8f73c109c91bd2f18faab4d6862ba33d940956d6457aaaaeeda5e8f72281edcc`  
		Last Modified: Tue, 12 Oct 2021 01:11:00 GMT  
		Size: 53.2 MB (53186352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf674df9fccabd4879c5e06d5d0e93ce0977242d5abe4ae7811fbd707df2cbb`  
		Last Modified: Tue, 12 Oct 2021 01:17:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b3c4fff805c799adaeb6f303688b2a506eebaeb4fa44b5acd62894106a1d5a64
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50860534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd03e682005cb71cf59753fd8cbe2ef48938f59f40dc27f2f581c04b0e63359d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:03:10 GMT
ADD file:df29fec66c741f67158d8ed2094810758d4a7cfb2c7cba3dbe60e5bc11ed824a in / 
# Wed, 17 Nov 2021 02:03:11 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:07:48 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:339de498e0e3324e5657ae3bd0868b26e4518664b7405a1fb321434233c56211`  
		Last Modified: Wed, 17 Nov 2021 02:19:45 GMT  
		Size: 50.9 MB (50860308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ece82fed24d30367e02d7e64c964b10ccfd15ac07fc7194004f021e5f5a72`  
		Last Modified: Wed, 17 Nov 2021 02:25:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4e643b87023ec376c041e087d96526b897466ff815c93e009c21822054991b27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54767270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef88aa400312f886965b74ff4049517b7b6ae074468393de39d842d82e0614c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:41:46 GMT
ADD file:6547698ce9c0dce5d390e739342bd015a0c3266dba4ef5828dc1b1a9eb46e826 in / 
# Wed, 17 Nov 2021 02:41:47 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:43:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:67eeb578521bba47ceed6d5c2de23409a33ec3c1c6fda03d83e22d74dc1cdb76`  
		Last Modified: Wed, 17 Nov 2021 02:49:53 GMT  
		Size: 54.8 MB (54767045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e7fcc41eba4bf5eaf90b91e396fbbd7e3419e82dd8276f76e396ea7836e08`  
		Last Modified: Wed, 17 Nov 2021 02:53:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:aeaa4cce1c7f6227141f7c026d4c44481a39095d516b6bee31553ecfa2b07ce1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56817038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429df637c8c5a34b60b89f6c6e168e89daf3773f2d4a09d5dcac3dda7d89ddc9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:41:30 GMT
ADD file:f85ffaee07ae67dcd7f97765e4cbdd725ebb7e06d7b05a80fc7ccddb5fda6b20 in / 
# Wed, 17 Nov 2021 02:41:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:43:42 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ec289c525481d0b14d52b85fde04accd67398f9603586e8bbdf75ee7b931219b`  
		Last Modified: Wed, 17 Nov 2021 02:50:49 GMT  
		Size: 56.8 MB (56816813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ff2b302b2f568b494f5434ff9f8ffed1a1c03892bd9b57cf5b3b759c7f6247`  
		Last Modified: Wed, 17 Nov 2021 02:54:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:4001ef350f071ae824fd2d0617f53b72bdc03ad21c9b2deecba4548c6aeb7153
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54365688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd50f42336e95b6becd718f780693a04e3b0bb1f118bbd4c7fa4d107ef8d4ca8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:12:23 GMT
ADD file:9e3985f5064204cf4c74f2d464977349398f8e0325083d223b22ace99f5dfa3a in / 
# Wed, 17 Nov 2021 02:12:24 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:15:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b79f1dde26df3dbfdaf094cc43f4dc602b492e9dd707f7a7874e1366808028c5`  
		Last Modified: Wed, 17 Nov 2021 02:22:36 GMT  
		Size: 54.4 MB (54365459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64772f0e563a3f926b08d5d8e37669aa7ff21b91479ae00635a3feb9bd2f356b`  
		Last Modified: Wed, 17 Nov 2021 02:27:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:8871ccce0b68b6b8e2f377f59816546c7757697c61fcea960b191e44ea775001
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59889396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16346dd33fc3f506b4950f71d8af23d5ebcffdd4a66f5776c8b9748d224f2f18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:27:58 GMT
ADD file:975422ef5390ff94fc050a84a9840e39188158f1c74f7b6dfde93829787b7c8d in / 
# Tue, 12 Oct 2021 01:28:07 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:31:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3794e49fdef56187e1a7ffe8a3c0d0dda8a5b5c159e370831000df5e5f638479`  
		Last Modified: Tue, 12 Oct 2021 01:41:02 GMT  
		Size: 59.9 MB (59889168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f376a4c7a802fa7692086dc3096f4d65493c272843b8ac365023df781c43cd`  
		Last Modified: Tue, 12 Oct 2021 01:44:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:6054ea59b35ef1d4279cd624e8d9681ef963b816a6e50612ea5119670b470c59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53965892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2d58825e5f75bcee91ad98bff0a56adad0030bf68f202a8b4ef3b1deda14a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:43:42 GMT
ADD file:ba3a56dbd46c1324142a33ad1eefa66c34fda8c9c635140debf01131cb259e63 in / 
# Wed, 17 Nov 2021 02:43:45 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3595b50e30d7d0d412c142596638dbf5abfc27f196fe5d138ded04b66fd2b50e`  
		Last Modified: Wed, 17 Nov 2021 02:49:48 GMT  
		Size: 54.0 MB (53965664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cddf6db144344852ad11c114803127e5c012f50bcfe344b2c9492160f02fb11`  
		Last Modified: Wed, 17 Nov 2021 02:51:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
