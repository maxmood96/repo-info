## `debian:stable-backports`

```console
$ docker pull debian@sha256:a6312f92a3487f889bf2abbfd6f4f2badfb0270921dc3368c3e017e09362a86b
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2ac9feeac45a5fd1be81b124f115609baf58e5a77ec7ea3b7a94ae439bb15494
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752685ce9675b4b65ba073d83f982faf1665600ea79508badd37ea6b0f98791b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:00 GMT
ADD file:d69b73f95cac930a42b91ed7f0f73cb83484100d69e0ebb9c47d6feef1771e84 in / 
# Wed, 24 Apr 2024 03:30:00 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:30:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f70ca9efdda4d28a921732364e4704f15c0703fe3a8cbede502b78466602092`  
		Last Modified: Wed, 24 Apr 2024 03:35:42 GMT  
		Size: 49.6 MB (49576272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746db019606ad9424fe312dd205406fc515530b8ba9dcb139c48cf0f64b8f661`  
		Last Modified: Wed, 24 Apr 2024 03:35:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3a8dde266ecf954b85d1c64022c67875be12a5d80924f01f6e39e4f424b6a799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d844e0133acc1fb49678d2b9fbd77b465fcc40027f67c77ffec73a1b56f5c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:54:11 GMT
ADD file:8bb086ef0b261e6c5b728a4f366005b71ec4f2ae9d60ae3496380a870624bb03 in / 
# Wed, 24 Apr 2024 03:54:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:54:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:daea7689f40ee2eedfb17b0c43b2ebbfe5e0c123d91903e4dd126b5a278698c2`  
		Last Modified: Wed, 24 Apr 2024 03:58:35 GMT  
		Size: 47.3 MB (47338618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cb2fc8f1f8b36e71ab1d7c5579d52177b4961edb46db8557d5874b6cd645cb`  
		Last Modified: Wed, 24 Apr 2024 03:58:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:92c394c81017e5f7e7a9016ee44a8ef76288855cf2171738c26c43f88db95a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45158826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac98c0fc503ffbc4163391d88077a121c2a7d121783a6ce2c118078898cb180`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:57 GMT
ADD file:f5a0b03302f0a5e8c1ec4eedfce83103c010d0ca252de78c1f694f35ddf10675 in / 
# Wed, 10 Apr 2024 01:00:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:01:03 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a5fcd6ce54c8e754be55f1c029cf0fd86edf219779922f7311173a5acb4541c1`  
		Last Modified: Wed, 10 Apr 2024 01:08:05 GMT  
		Size: 45.2 MB (45158604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa161395ff1514b2b1f1dbd038f04da32dcf06801825abc325cece605f10aa3`  
		Last Modified: Wed, 10 Apr 2024 01:08:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3b706b7aea42de94e9c379f15d4b0fda2e7d8480c15258d3d1032d84bac65abb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49596484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b9a307693b8d6d9a69a10441364e7f2c738aacdbc96f94c4ad15593f9d584`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:44 GMT
ADD file:dca6811bc1b65e1fe54cbd2ebad57417e39ba29bf53af1fe0a5f64ed79912342 in / 
# Wed, 10 Apr 2024 00:41:44 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:95cba99d2ecd28260b5e8fd2d88c68996d94c735378ad3e804351a03f15ee7f0`  
		Last Modified: Wed, 10 Apr 2024 00:47:14 GMT  
		Size: 49.6 MB (49596262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05785b146fa382f8df3fd693de4cfa93e29b12b2e26095f7dfe1fa3f99edd00`  
		Last Modified: Wed, 10 Apr 2024 00:47:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:a3df1bae3a6b8812ca29856ce697ec4f70f23f8c54d0adc0d4a7c333935d8244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614f6394946eb56783acff2a5ce3c5fc8be893d27b9082509c4905a15159f020`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:40:51 GMT
ADD file:c0e69ebeb06a792f806f203b15627c6edaea11631becc2060e9831cde85b20bf in / 
# Wed, 24 Apr 2024 03:40:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:40:56 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c415ea9373d4c4c856ef6ac5cfe9976721b24ab161a2460c17bfc27949a4cd33`  
		Last Modified: Wed, 24 Apr 2024 03:47:13 GMT  
		Size: 50.6 MB (50602609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0ab3f5e4402e4231f8068668c2f90656d181b1d0414b266dd8081be701071b`  
		Last Modified: Wed, 24 Apr 2024 03:47:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:c4acd7b782c7838fe4cbc9ced74bf5c2ef0d03f899df0ee326f4ce552a9c2674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49583028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb759f376b558f07cb63d28df9b05840299bf5fc788d1bed56a0bc5ff6bfbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:18:28 GMT
ADD file:0fc3a29fd4805efb8fba8020dccab3b1b6fc2c0828c9ead519ac7a16c4eb5cab in / 
# Wed, 24 Apr 2024 03:18:33 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:18:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:48bc9e8cd1d92c59f529de438a611bcc91f7735e8b62e60f69baa2baa57d7e5f`  
		Last Modified: Wed, 24 Apr 2024 03:29:53 GMT  
		Size: 49.6 MB (49582804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525626e950f29eade5a5536417c60e02c98185916e7b797459be746f3231258d`  
		Last Modified: Wed, 24 Apr 2024 03:30:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ad6f6694869aef64616ffa437b609cff08a51e4a9a845096fe0ecff29ec7929b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53580344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14645a47f84f9cd416a3463f03fd38ec09a06ae8afb008e49ceef5bae7ea0e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:55 GMT
ADD file:49b92159424eb973fa890025f1a59cd18824358e23e55a092257c2c3d200fd37 in / 
# Wed, 24 Apr 2024 03:22:59 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13fc0cef51b1e2c4b5ca78eef06b6140164a8ae5974f935e21c932e74592c6d1`  
		Last Modified: Wed, 24 Apr 2024 03:29:16 GMT  
		Size: 53.6 MB (53580119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc739ad9659b73625801d7cafef5f7ccb9ecc9d14c91d7cc332fc1e5ae0a1ca`  
		Last Modified: Wed, 24 Apr 2024 03:29:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:2673ef08e05121a4a73659c20dd6057769488e94ae7a40e5d560f50fba46504d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f391dcff148aa287baad6a898507866441180f4ba7e8be5e1693663e8f9fca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:45:37 GMT
ADD file:cc009ea5f89b4a722bbc3faafcfa98e37bf7e4b529f4685a797cc10ed306c3ca in / 
# Wed, 24 Apr 2024 03:45:40 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:45:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bef015bfef6c3e2e79be5ea0dc66d68b346787645a683fd9bed97885f9ef6643`  
		Last Modified: Wed, 24 Apr 2024 03:50:50 GMT  
		Size: 47.9 MB (47942181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a784036cf729dc7933cbdbb3e321dbefaf70bf368cbd1ed3da89f287251af5e`  
		Last Modified: Wed, 24 Apr 2024 03:50:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
