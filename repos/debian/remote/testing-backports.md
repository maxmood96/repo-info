## `debian:testing-backports`

```console
$ docker pull debian@sha256:744b0996502dc54448302e63150d143c2a9281a31efe4116b8d481f403142a66
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:234fd9e64a3c19844eaf741b84f891d962c941f1f11caff1816c4b9b1ce487a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53153161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0bcaf2616d16c18df83ed5fb86b3c2a1d750d3301d617eb7927136c421aec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:17 GMT
ADD file:1fc45771728eda64de7376c84e22e736076b87ea1b407f029597e49a03bfe372 in / 
# Wed, 04 Sep 2024 22:32:18 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a0989ecf4472e2d3327e122cab700e70a9aea1e22dbc31b893c142eebe6cc665`  
		Last Modified: Wed, 04 Sep 2024 22:36:36 GMT  
		Size: 53.2 MB (53152940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5560c124ea0daaa63f3661bc68331e7eeff9760baf7e91293cbed1e018efbd6a`  
		Last Modified: Wed, 04 Sep 2024 22:36:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7266d469c5684e64fdc4771279e8c92c1cef612c293a592fc4efc5b55aa07ebb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50107295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4776fad490aa9f15fbe31003e87c225c3eaaa88f581896fea262c5070dd80c98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:43 GMT
ADD file:1aff6dddbfddcca844322bda5bfd098a855c07d34fe5704dca7171f5c1f56ece in / 
# Wed, 04 Sep 2024 21:49:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:49:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a50fe0a1bbe705d3679428469219f780f9136db589d5f4f8595d79515abf6bcf`  
		Last Modified: Wed, 04 Sep 2024 21:54:03 GMT  
		Size: 50.1 MB (50107073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a295897e198650ad0c8c7425f41f8695b5e1c319d03971703ae5b389a537b158`  
		Last Modified: Wed, 04 Sep 2024 21:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b5c8fb0e94a8b6efe85e57869994cc665e8bdd36a30acaa0543d434a2b5e94d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47600589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc410bba7a5b4723193879edf3f122d24b281113797957b2f11320ba9ad6834`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:37 GMT
ADD file:58e7480ad070c187e966d1f49cf6bfd6820edf36f8bfb4adf8cf4a7539a92063 in / 
# Wed, 04 Sep 2024 21:59:38 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:59:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:95514cfe4ae89b3874639f2bbaad4efb19ac5fa1f1880dc900f00a4707da1483`  
		Last Modified: Wed, 04 Sep 2024 22:04:20 GMT  
		Size: 47.6 MB (47600364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffc6b76bc413b9321f0cebb3a500eb19b2fe5b40096e23161d4d3bf7e45afc0`  
		Last Modified: Wed, 04 Sep 2024 22:04:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:259de614e5adbca203a3c5656e9cb3bcfc533c70f3969fa4f572462e9e963b0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53594580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a31460be948ad0030a6ba35a8ebb75086127f10daf07a542ee72d3a706c1d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:57 GMT
ADD file:394779f4486ebaf8490ab95548a898d31798f528981c6abde9a64ae9541ad916 in / 
# Wed, 04 Sep 2024 21:40:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:41:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1d833a2b98580c8c6fbc93eec4d1f948a740704ada36d9bfe4881cc92113a70f`  
		Last Modified: Wed, 04 Sep 2024 21:44:46 GMT  
		Size: 53.6 MB (53594358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7651c52de501fd52bde87e9099070ac23c277073f556c906021ba9535f210ade`  
		Last Modified: Wed, 04 Sep 2024 21:44:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:ea9961279bfa6150470c8ca04140d14a7c71dd55a9704c792a402a06221b063b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54024489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a749a171ce50cd0977e5a378487d360881216f38a590340f12a79eae0d2ab018`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:07 GMT
ADD file:0fc6bb2c2d834994abff10259e23033c8986cd73484cc8f57bb0010f634d57cd in / 
# Wed, 04 Sep 2024 22:46:07 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:46:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:716214a7650a904a011161c59556cdbcf47abba341c6cfd5163da0ffc9fd7687`  
		Last Modified: Wed, 04 Sep 2024 22:50:53 GMT  
		Size: 54.0 MB (54024268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6064123e551e4278274878883f4a99230985ae1e05d71ef8eef4fb2932540df8`  
		Last Modified: Wed, 04 Sep 2024 22:51:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2f8bd58bc7bc062b14471ab6c66a6bfd16ccaaf5f0210563c5867576d1a5cb90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52218646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ca0e88af8a6d7f96a3466e6403cf8e5dd5c9ef445601ba19c1ce3ae8002514`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:18:47 GMT
ADD file:c36c80ea02568189aa3e85f8072a712f381a7231dd4efdeb5737ea44bf812876 in / 
# Wed, 04 Sep 2024 22:18:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:19:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79d5c9efe01709f7e899d8d1b6c857c73fa6bcf862f4440fcb296993dcf36fad`  
		Last Modified: Wed, 04 Sep 2024 22:27:16 GMT  
		Size: 52.2 MB (52218422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb91120f20646fa84de82d445e8b17435cdbd6567a1d4552085f1009ec1b02d`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1443748e880daef042c8161c997e943e8e1bf8a667b1cab20f86f49a0b9218aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57077990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550a6e8986776dba50500118ac82e8603c90d3dc92f12ca000de8167fd3299fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:27:46 GMT
ADD file:e76ca2322a73a59209e43148c51a8c79f7c3e572eff94a2519628b16edb02b11 in / 
# Wed, 04 Sep 2024 22:27:49 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:27:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3b2659f6b1aa74a9122222e29d09e5d1b06a1b6eadfed4e19fd744c16754d022`  
		Last Modified: Wed, 04 Sep 2024 22:32:58 GMT  
		Size: 57.1 MB (57077769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39199d7e99ca92e2f03e36b4067784f021163201b568056dd5ee2bfde7adccf5`  
		Last Modified: Wed, 04 Sep 2024 22:33:06 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:c5c85d87f9b98231911887f5b6bd8971bbcefe87f2d8279a1356368fcc8aa0c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51475755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e1d2d4c5270955ab9b547bd45e4fd06f87d87b96786b22f64c0ce658c7c070`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:48 GMT
ADD file:8af277225e65f8175288ecc8586a6222e16bd50188e97473bad54f94e4c177a4 in / 
# Wed, 04 Sep 2024 22:26:50 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:27:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:934dbf213425c83bf8ffd8f4b0231c081388d35c0108cb1f47338fdd8c4fe172`  
		Last Modified: Wed, 04 Sep 2024 22:32:26 GMT  
		Size: 51.5 MB (51475533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d2ea2f28c6bbc836f272437123387dd318b6d45efbe5df5d41d99417743361`  
		Last Modified: Wed, 04 Sep 2024 22:32:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:b5b11fc830864310f26ff3b8d82a2216defd977b66fcc89fb7ca669df575b13a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52746701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d825c97cb5f6fc232bddd7fe36a9d331248943bd4b876c5f13562dba53b5499`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:05 GMT
ADD file:59e982fbd6b5364ff9e3c3a4656bf6cb6795d637a02c788e4db61959964e2b65 in / 
# Wed, 04 Sep 2024 21:45:07 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:45:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ff4f98e3072ebdb612b0732715fb700fbfdf55f51351132742a0b343fd7fbfc8`  
		Last Modified: Wed, 04 Sep 2024 21:49:29 GMT  
		Size: 52.7 MB (52746481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9d15d8ccef68b03dfd0744aed04e68b335a892560e79b98cf9cfee1a5a2cac`  
		Last Modified: Wed, 04 Sep 2024 21:49:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
