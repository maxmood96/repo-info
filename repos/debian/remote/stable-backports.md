## `debian:stable-backports`

```console
$ docker pull debian@sha256:e1bb3508da2c8fd901c48c13d8060fa3d0cb6ed5710600eab5038a474e82bebb
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
$ docker pull debian@sha256:7aefede0f9100a63a487a931c67bacee604459d9dbef84ecd210bf9088c586b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070bbf307f4a89bd171d9e29dba4e9fcc6fb60d32eef1426b89f5480f47967c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:36:47 GMT
ADD file:44c36edaeeffd19fff730379371c1494ed67a46554cfd7cf36cd287125f74c25 in / 
# Wed, 11 Oct 2023 18:36:47 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:36:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:98d7f57ba43346ee07b85d15fdd663e748330ec597fdb80bdafc474553e15128`  
		Last Modified: Wed, 11 Oct 2023 18:43:00 GMT  
		Size: 49.6 MB (49582232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5f5219b613a2d18e8f61a761e5015842e03d433256fdb459d24e2b48a673c1`  
		Last Modified: Wed, 11 Oct 2023 18:43:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b7a2bc1e9a3e9fd05609bb5878bf03b25fd22a5f360876cc1ed26ce381cdce53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47355986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae279f4fa206f8642a889eb2b0071a2377b1e1f97cf04f1b149ee44d12a645a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:38:35 GMT
ADD file:3dfa21483214d6fd6973bf5ea67b9141553d9c57ab18dd58be011147b89db505 in / 
# Wed, 11 Oct 2023 17:38:36 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:38:38 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41dcea1ccb0cc2ae430dcfcf53e7bb28141a4c89547aaa5fd95c63c233cc81dd`  
		Last Modified: Wed, 11 Oct 2023 17:42:58 GMT  
		Size: 47.4 MB (47355764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc23ee2b798f6caae09687bb231f0d82fb78626c37bf96bcdd7ee1701d4238`  
		Last Modified: Wed, 11 Oct 2023 17:43:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d4344ae77e079fa9b564a2ffc3771cafc3a6de3be8b34ae903a4a409f1505148
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46f077b1a66b5a378ff26581eda180a55e73f3c116cb3775d81cea4f92f1ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:43:49 GMT
ADD file:def114a3538bbcfa27a4ee203f247cce6350377fe1dbfcb49bab3a6cf6b13c94 in / 
# Wed, 11 Oct 2023 17:43:49 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:43:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a10bb75b0a43fc3e95263c414cc196144041906e596ee2d10115ce43f5937f10`  
		Last Modified: Wed, 11 Oct 2023 17:49:47 GMT  
		Size: 45.2 MB (45180281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc67b463fae0b44ea0b0c9e83e76a6593d4752a56142c715736aca1efcf85a4`  
		Last Modified: Wed, 11 Oct 2023 17:49:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ada3024b128ab5bb4ebdddc154c4b62e8bc0e1389fc0bb0616b10a6f1d87e269
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49612773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75b39e09c72a31b1788c77bf5138ec7008f2b6aa68a6fd0ea8da272a6cc8b4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:26:08 GMT
ADD file:ede730e57a20f4965f2bd7059f0ecfea4a76efdcfa2cd3ccc120fdd0cf0b6417 in / 
# Wed, 11 Oct 2023 18:26:09 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:26:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:12cd1a4d0fcbf9e6a142e3b55f53a6900e0300e0582acbd1ecae58b7670779b8`  
		Last Modified: Wed, 11 Oct 2023 18:31:38 GMT  
		Size: 49.6 MB (49612551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b35120e4e7fb375d25ba47c71c50b2d73e1634706a81971c10f8d54ea7f586`  
		Last Modified: Wed, 11 Oct 2023 18:31:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:2c1a4b0b9c8ce61b1ae4bf000ef65d39d21f3b8b845ef46d0413420076e918e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50600967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b312b99d343d3d9677c0bcbbada967e89e28a3180710accab8e0613aaa4a498d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:37 GMT
ADD file:6168d4b38f14ce4fc332add3f9a40d4651c7d3fc6307b4b12fbe624ba851d20a in / 
# Wed, 11 Oct 2023 17:42:38 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ee03d88e8927941b8f5c665d5f66b2e72b9713e22546461226216d3f9e0c2cf`  
		Last Modified: Wed, 11 Oct 2023 17:49:38 GMT  
		Size: 50.6 MB (50600744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d48bb7401057875843dc5843f343690625447079ae6099e73b7d5d34e4f61`  
		Last Modified: Wed, 11 Oct 2023 17:49:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:276b5b53bcf8389e26490a6b4e527bdebef9b32447c3a528fe17219808bb8bfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49569447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcaaef1884788efbc56791c420ee31a1ebe393fb298574de96b656a4cb7fd92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:53:48 GMT
ADD file:f4ff25ab3d231ea582babbf4f29165c3f65291434332b047fa2d41035314a14c in / 
# Wed, 11 Oct 2023 17:53:53 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:54:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dba2f8ddfe5caee1ce4991c82269145959dd91d33f8f961efed3aaaf3f2b2deb`  
		Last Modified: Wed, 11 Oct 2023 18:05:13 GMT  
		Size: 49.6 MB (49569221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81863ce58a2fbb32e081d3f63bd239eba2b8ffddc9661442efc7b066fa5d351f`  
		Last Modified: Wed, 11 Oct 2023 18:05:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5574e7dfae11555996699279528877bdafa1c2a21216907389297b0ff67e1d90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53576187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd8f3d2d59833bc5dbfc8a7c5f558892cfe04fd84a360df4f37528db0c2c48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:46:14 GMT
ADD file:6f01471be4c62302b72e885495b3b47e7744664c11e162b97c2aa2e6ec59793b in / 
# Wed, 11 Oct 2023 17:46:17 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:46:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2b4cc8711faf88be58a5dab9e7d686aefbaacdb081873031cf190ad2325ee1cb`  
		Last Modified: Wed, 11 Oct 2023 17:52:52 GMT  
		Size: 53.6 MB (53575965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3551cc446bbd94f534dee055b87dd720b14c930126f72a995a67244b592b61fd`  
		Last Modified: Wed, 11 Oct 2023 17:53:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:a55f90daa7b73dd38991cce6798a0cc0fffafbffc1ab275ee58c767aa158e054
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47943177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef754df2c8f2efa4dfd61686caedbfa9027eae444106fa353921e511ae6b920`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:52:09 GMT
ADD file:9bdfe45aeecbd072e199f7d8fa443992573fe8dfc7d3f534f1cb43eba5659d67 in / 
# Wed, 11 Oct 2023 17:52:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:52:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:87a37cff3abc315812cf54485b206845e2a4fc1f3d87ca7f1d1d2ec8d930a47b`  
		Last Modified: Wed, 11 Oct 2023 17:59:41 GMT  
		Size: 47.9 MB (47942952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65289eeb1670b59b475e65f88850886658df50ad01b38780b2cab5bde7e1670f`  
		Last Modified: Wed, 11 Oct 2023 18:00:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
