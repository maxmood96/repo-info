## `debian:testing-backports`

```console
$ docker pull debian@sha256:a13f1276243a27ed1a0fb2d2ce52053f864846a23a3555b7fb1f80708b75b8d4
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:554c782743a2cbf47b879b87ae60729677270409d1accb6f428c3709ab0abcf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e32cd42b8c8a0c71cc2ed56db0a7c5691601e241e6f7c8c38a303de06ab5678`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:56 GMT
ADD file:ef0363530acdb66060536a24b4c64786db9f35d1224e1d13645c9e15a1a5a352 in / 
# Wed, 20 Sep 2023 04:57:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:58:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd55a40fdbce1f8af26c95e5d3ea6a93b913082fb16ba4a530d076e6527a3172`  
		Last Modified: Wed, 20 Sep 2023 05:04:15 GMT  
		Size: 49.5 MB (49467667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59c30b8f8f8a49e55d7635804c318964d4ff6a1f86fa6d16fe13a8d1ca3fe3f`  
		Last Modified: Wed, 20 Sep 2023 05:04:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4c79613517abe0b6753dd081a75b4f9c33c5df5a47eabd4f9c655c2084e2c1db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47170302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216ca37bd7e82b592f29b7ca783caf13482949a3c6cba6d439dbfb6942639a27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:51:53 GMT
ADD file:c40dbacd84c044a6cc84e52a992d1b1d5966a49aac6d3218557c6a7f82315abf in / 
# Wed, 20 Sep 2023 00:51:53 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:51:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3b42eedb8ee5a76839537b23b1a4cd51deefe233d9b4985c65ff34c3ea12831c`  
		Last Modified: Wed, 20 Sep 2023 00:58:07 GMT  
		Size: 47.2 MB (47170080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fe964b42eb583bce325bce4226b39a5fb352570aa73cfbc7aa13562a733119`  
		Last Modified: Wed, 20 Sep 2023 00:58:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:83b867c7791ee754064ffc4238fea3c912ff8ad4b021d4bf52aa009a954fdecc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44955307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0d138d03a92e469fe2a07b3369b0a4a832a3d2790a419b6614816fefe988c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:59:14 GMT
ADD file:c3fc371f29a882e3cf9a9cc75c794c8e4cd6abd5d27b7e8bab9a04b769ba2560 in / 
# Wed, 20 Sep 2023 04:59:14 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:59:17 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c555a284463d37dff856c2203882233f87285b4a778176b2233e53a594322b16`  
		Last Modified: Wed, 20 Sep 2023 05:05:05 GMT  
		Size: 45.0 MB (44955084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984aedc5137b0fd82bfa54b0d1674aeef854354e0170478e231bb2d12c3d6fa4`  
		Last Modified: Wed, 20 Sep 2023 05:05:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:181c8c60a8afbb88aa675d0bfdc76e801ebcd217522368a9cdbd66faf8a262bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49404752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d346454a93ad1829db9182aeef2bdb8b01c2f026f6d6c74226b179bda0710b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:43 GMT
ADD file:f0c1d15ee705796bc58abf92f15b7a16aa341028b6e099383437710d3694d315 in / 
# Wed, 20 Sep 2023 02:45:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:45:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c80309e0a5bbe8e3c8000103b383c6a60c58a6a84681e6aa5963d565eebe59a6`  
		Last Modified: Wed, 20 Sep 2023 02:51:00 GMT  
		Size: 49.4 MB (49404531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28a7bd6548127d0396a249571cc55f534c820732c903340e6fd755544ceeefe`  
		Last Modified: Wed, 20 Sep 2023 02:51:09 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:c83516da0c19744d493a6b4b7c32e7d0e3458f7d33dcdf1db05ac1ff616180d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50484976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45b2077d5fae3005d43b34884fe4b8c60c3ef9dec14199b1bf07d6979083eef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:44:16 GMT
ADD file:4d59c3dd2ca4ba5032a14346c8fdcef109b7734aca831c189868d19ef506e4ef in / 
# Wed, 20 Sep 2023 00:44:17 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:44:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0c50117d452a905428fa6728201904b2d7d1008e53c0be5357dc3e3d79904b93`  
		Last Modified: Wed, 20 Sep 2023 00:51:18 GMT  
		Size: 50.5 MB (50484753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc3a7e370a360c1fb11c519270fe48b8381680de65a6fa7b2adcf75857e12a6`  
		Last Modified: Wed, 20 Sep 2023 00:51:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:02d49666d52f688aeddca66dabbf97ca5e68564bb2047ca57954186558f59f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e21e18e60a5b951fdacccde54d78d3fc74b21682757373406590be418ead42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:15:27 GMT
ADD file:c279daaece8cba4369dda08fde64059093b805e0480e5d49c2ebd6031a4c3996 in / 
# Wed, 20 Sep 2023 03:15:33 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 03:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41b75db22e5e70a0b45e80eb89c31691d77bd206c097f08afdbc84713af36684`  
		Last Modified: Wed, 20 Sep 2023 03:26:49 GMT  
		Size: 49.3 MB (49302333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ec506c33c33d3ec0d6a625a3fc186a782c08ddbbcf4eb36b5e71fd5e0a6dd`  
		Last Modified: Wed, 20 Sep 2023 03:27:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5f47e5ac0193ba73918ba0a7a89711ddb5c456a6ad400b18bffabffe36093fa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53395529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2d4d79429ede3fbd3b13fb804f1af6038c940f1bf44ee4e30289ca8a9209d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 08:47:00 GMT
ADD file:3f9069bedf0a55742528dce12a4b55dbe06ecd03a163362a22ec262312f78e63 in / 
# Wed, 20 Sep 2023 08:47:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 08:47:09 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a30d0f3b9cb815b401d94b7504a260d701d1ceed70755bc25e7ad79803a36dbc`  
		Last Modified: Wed, 20 Sep 2023 08:53:19 GMT  
		Size: 53.4 MB (53395308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee0883c067f045d1955c16539792a1f572a14962536b79be8476e96a5c0e8c4`  
		Last Modified: Wed, 20 Sep 2023 08:53:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:9fdc21b062b1f4a26127271939c927cbe60ff3b86b4e1e2b9f5ffbe2a8821b0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9137e794fe37e14ce2041be00ebd8a2e4c949bc1e3ed74f8828aab77f58eab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:56:53 GMT
ADD file:55adf3f3f6b9fa65711565f1c1946ce15e33e4fe2555b494fc36ac99ffa072ac in / 
# Wed, 20 Sep 2023 02:56:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:57:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9de78c172a0d9b73fefa46bf099a36fd6685a84a3d5085bc4bce9d9878f7f456`  
		Last Modified: Wed, 20 Sep 2023 03:01:52 GMT  
		Size: 48.8 MB (48760809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419f5fca906dfc6e89ee84715ca2ab73d0a95da223f490c156832b045efe966c`  
		Last Modified: Wed, 20 Sep 2023 03:01:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
