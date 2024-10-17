## `debian:rc-buggy`

```console
$ docker pull debian@sha256:2acee9416ee50af45825677e61db51b7ceea329595b8d7334228ccfc9af3f092
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
$ docker pull debian@sha256:94eda6771c55d0c3619b329e901b349ee21c5f9626bdde828431aed591f2194b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1762de392a1548d422e32f58fa85d2f179b070537745b0d216c0fa7da9c25468`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:22 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Thu, 17 Oct 2024 00:21:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:23:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e263ba096289a2844bf39669b475de009f157519e172fc468f4dfe2ede16628`  
		Last Modified: Thu, 17 Oct 2024 00:27:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:a692b0ff12e9022f99d084a573bd1bd4afd31e94824802c1b2739741f07a663f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50147809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcf7d70742fa7d6f12987299175b98ea629e5d2395102cc7a0c3b5f35fca1e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:41 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Thu, 17 Oct 2024 00:54:42 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:56:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a459f6360e2bf91f40b708330f548dcb15395b373695b1d433ee15f0242804b`  
		Last Modified: Thu, 17 Oct 2024 01:00:32 GMT  
		Size: 221.0 B  
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
$ docker pull debian@sha256:92044a9e25c84f67cfda2ec3738c88858ae4926a3bff89fdb102aa8c83008a17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54118199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26022125b843dff54aa1c7b7ed44632c0aa12e5e174a466feb1cc0ca9e12969`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:51 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Thu, 17 Oct 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:41:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4652ef0bcaa9f12c2246ab532cbbe42caf2e2e28f45cc6a97e28afa253a8ca2`  
		Last Modified: Thu, 17 Oct 2024 00:46:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:692e2387e543a26408a80641a0335a14b580fae0cff1583b259ce9c776193f93
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52125804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6742b6d2b01655f65f3efdb64cd937b4f0e2f644b7a92b611e61fbdba1fce141`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 09:09:52 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a99401b2edb1fdaf8200abee229920e5eb42ab41741e6af75e028ad13660eb`  
		Last Modified: Fri, 27 Sep 2024 09:17:54 GMT  
		Size: 226.0 B  
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
$ docker pull debian@sha256:e984eef5109cfae52526a92e18f9548c1d61113b44f9d6bd8ec04c819e53391a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51526295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9947c4f46d6ddd311c1b91bb40ca1833350a02ea4a2df0282b7d9d777c68af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:24:57 GMT
ADD file:60c08991ed6d648cb7220494e8e535efc29df9008317554c36bf5396cbdeafe4 in / 
# Fri, 27 Sep 2024 12:24:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 12:29:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5817b4e976e9e9f6db4fe62c9c9fe0f00a2b6fab03512e0faea17d129e7ef265`  
		Last Modified: Fri, 27 Sep 2024 12:30:30 GMT  
		Size: 51.5 MB (51526068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a29957f80d6d287b1cbd3b47eab1add4f98c45368ffd558c7c65b148a43330c`  
		Last Modified: Fri, 27 Sep 2024 12:35:39 GMT  
		Size: 227.0 B  
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
