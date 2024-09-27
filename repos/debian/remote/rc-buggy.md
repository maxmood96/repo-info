## `debian:rc-buggy`

```console
$ docker pull debian@sha256:6bd7058fcf913a7b0fe911ffda64f7ce3860e95e5044d77adbdef595d5368e45
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
$ docker pull debian@sha256:8a677bcc24a2aabbf7a0e62e61da0bd49a51cd7b6e0e5ece60691cee9d34985e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53250269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c92d46d9b0607cbc51a2e724f250f4f44d9aaee333bf10596941282cf5a9d55`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:32:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b95ff1e7e900913e164d221bb3440e9aae2eebe15b448ae5d0f0602b48f97e`  
		Last Modified: Fri, 27 Sep 2024 04:36:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:d815fbad9b48de4377f76a12e6349dc2dcab87937cb814a97f823ed13cf56e57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50141410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203685d95b81e59e76890942e30f240851d08473ed99ff2f3558f1070d660de5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:20:53 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ceec838c24ef5b22f496aadad7625e4bbae6356f15f82d6bd1d378f168ffca`  
		Last Modified: Fri, 27 Sep 2024 03:24:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:d14d56bb243c209d5c2afc0f475697374e70fba36576ea7a23bf6d4a446faa64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47657114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bab8a7570611b185d2bc96d7c9a4e0bfb8a373871e3768557d2a425243cf7e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7f0525a348dbadad7dfbad67fa16d746da853af6690b84b9931b9c5aa3fb58`  
		Last Modified: Fri, 27 Sep 2024 05:21:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c9fbe9259417e4d75ddad33a9dcaf8899f1d9919163a4c696562abd8bee28fd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53594489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dba90397487757b86b512f52b229d162995d06334b7d4a8609f5a992d74f71`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:40:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbe732fef4691444b8ee1526db7e45222d8da2bd91712f3a79c7731df6c9b0a`  
		Last Modified: Fri, 27 Sep 2024 04:44:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:50f6dd23e0b2be6a6e9bea9472a302ff5f4abf5efecb9f46551c9c01e33e6629
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54078035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336595035a8a619d5be5663121e61245a2dd3cbb2c824aa98a761c3c2c43c161`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:25:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99f44a0367821066e5aa6f1eec544880f5fff83c7e1ebb34bceea9de80cb316`  
		Last Modified: Fri, 27 Sep 2024 07:31:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:d69f9fb87a33713abe0ad1f6ca4581dc7cc852bbbd4d2bb6f45b53d4d71f549f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52121302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf37fab2a491a32e828a12f46f512c1ab9f6f313d9cb4f5ace24305b6e779ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:22:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6935ed18b2ba8ce82d7a68e7e98692ba582b3affdd40b012f0670b38d89ecc`  
		Last Modified: Wed, 04 Sep 2024 22:30:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:cc2252696877faa5e0e5f801ac013ce510e20376197ed49fa5bc960d3feaddaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57123387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e174330edba7396a42945668e040d9685668ab0a58aadf1b07b15f780a0543aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:35:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8362800e2d4493c6b1a5ccb90723c21f0019d05ecbc5936d8ad803fb9d20bb`  
		Last Modified: Fri, 27 Sep 2024 05:39:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:9960c7f43044ff0a5ac6aea01f00ce5210b1bd3981d693b481d5ecf50d54be7e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51474081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed927086a9230c0e687ad0726fd59afbfcc6a988844efef3a97821b7bc3b42a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b9acecfeb10367a53293de4aca7b22eb21ebb799aa3404405682cff688f98f`  
		Last Modified: Wed, 04 Sep 2024 22:35:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:f2647cc61eaec57e719486c03c4f8c68864bcf633ae03e5336a38ef42c1b5ed8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52808367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51daf818376f357114738f0760813860cecbb2dc34e3ca9577dbf10fceee01b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:46:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b387dd58d93846e056a1b675973738d691bba2853dda6dc95fa9d8291edbb4a`  
		Last Modified: Fri, 27 Sep 2024 02:49:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
