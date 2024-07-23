## `debian:rc-buggy`

```console
$ docker pull debian@sha256:37e12b4868f0d2a5884b53430cd42db109c0a31cc4fc57d518d63ebd5a7f4c2a
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:e681d65030ecdc1d81861c05275451c59833b14d14656ba5f05986087ebea191
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52634796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98feb0e3a55965942ded4d5647d50cf8b834a6defc5a34015f1ceb6816deb5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:57 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Tue, 02 Jul 2024 01:25:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:40 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91094bf032ad28b8220f73a02b948b0b67d5c0a918e77e332865ee54e66e1e7f`  
		Last Modified: Tue, 02 Jul 2024 01:32:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:c1b0937b24896baf5a0180b058eeaea49982dfcf2d651599c062c85e2c11b519
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49829081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ea27c959c08ecdfa901fc4ec2c3b1d59566b08455204ddf37e3d5d167dd12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:59:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783c6343481b1aab2ce8620fef6a5fea33b86e6d6109e5f27d6130c922895cf5`  
		Last Modified: Tue, 23 Jul 2024 00:05:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:ed629e6387a0144ebed0ed9f65074e58dbe6226dc144af39747a823b07083e5d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47312206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c02418ff6b40030d7c5301b11eb8a18db680b267396d592b663b220e9fef54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caa5adaa29cfdc69bb7a4947c1db48357f2e39a0cce9567a8e189ea12863bb9`  
		Last Modified: Tue, 23 Jul 2024 03:11:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d31887cc3b135d3a2c70c04cf5e7ad2fe51c291cc5bf317bcc0f466038e8ffc1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52888982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae2970deaf2c64307b3c4ac4c0e8b6fed5590bbf877e891954eb8cc8492775d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320ddbf3f0b65fd9902a80dc192a3a05da430039f5fe2a61179bf7bb54a8516a`  
		Last Modified: Tue, 02 Jul 2024 00:46:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:eb5d1bffd5ffaf09dd2629890bcdbc65937df14d1578a61f0c0f2d5b761ea844
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69265477c0234d1c2b85392281fd4310e92efa019afe0b05d7cd870a6bbae0b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:56:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f976ffcd2aa63b3198e53aae70c1dfe754c8e2f3246cf94991fe15f3fdaf5b`  
		Last Modified: Tue, 23 Jul 2024 04:02:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:c27db59b690e7694af4cbb7f03555fae06552f8e8081e97c5aebdb7759fe49d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51646781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9285d433e5e6334848966282779397c4f7114c5905a568ab5adaad3111de73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:47:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d6db3f9d0575107bbb2806f4f340564537e7a318c5a0e406a24412fb5e909b`  
		Last Modified: Tue, 23 Jul 2024 00:58:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:e3db7c91d8c5de02f3bff9593442e012ba9f0538be248c65da756849fa08292a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56726696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7ebb3099b933d94909c1e657294d920dacae647b9776676b7acf6ad255e97c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:30:08 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46f668e08bd20fb8d485bf06671b289708b074170d7c8aa5da6ff39a2d0fa75`  
		Last Modified: Tue, 23 Jul 2024 01:35:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:e7d8710761445c08f47066ea517f1b447db0230c3eb66f4ce42970ef2efa044a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50937377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4404996351fb0be4934c668c16a4bf53dfd5bab1ae4dca122ca27b542d2ea80b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 06:00:05 GMT
ADD file:cb8450d273e9ca21e77fb71fa8d82d31fec1f23d51cec9972814bdc76724935c in / 
# Tue, 02 Jul 2024 06:00:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:01:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bdd8e78a3c764042cf6937012c6bcfab521fa52691a33dc6b9d4a6306b03976a`  
		Last Modified: Tue, 02 Jul 2024 06:02:52 GMT  
		Size: 50.9 MB (50937149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf8c2787951018b599f2fe45c7b602fb869d7055657f68f3aa9d15d93def8d4`  
		Last Modified: Tue, 02 Jul 2024 06:04:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:707e2ad474b0b5b9dde1e26d24ba32ef672de5d4407265db244f4adff751f638
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52435722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c6ef537a1f6bc888938311ea4e8a20a95ba5c141c3d3a18db1ede6f51a7458`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:31:48 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1cdf0a0e982343c03179f618f89642d066d5a047c01a01dd304be249617b25`  
		Last Modified: Tue, 23 Jul 2024 02:35:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
