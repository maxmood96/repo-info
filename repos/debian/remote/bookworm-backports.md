## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:f757a7edbac02eedfb3a08b217d94d2162ca0d3eb2e40acc087fddddf5852bf4
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:6445ecdf4c06ce88d54b65b9aec705a63ec5dbe031520fa1759a10699014ab85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49560584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57493964effadbc2f12f1b7aeddcee0a009f9a03183c9762b7101d5707f59a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:50:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e347f859cd2ae5c318c8ad5994f832f52c56cee7f740fe13bb82a3b3567f52b5`  
		Last Modified: Wed, 10 Apr 2024 01:55:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d23b95424befa4fd8e5e0a9719159a8c96d4f23cc2a849f80e76164a225c51a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47316368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278b671b6c1a044b96f8af6ee211c52c81286c46a82118997c73dfffae265b17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:48:43 GMT
ADD file:b0965dc0b90d6c10055f9e01eee401939303a005eff01dfc0ac17671ac10c89e in / 
# Wed, 10 Apr 2024 00:48:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:48:51 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:db9b031fc6f21cd210f5feeda489a6e10c26355e778fbdaeca7ec9da4a730942`  
		Last Modified: Wed, 10 Apr 2024 00:54:05 GMT  
		Size: 47.3 MB (47316142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b89c8bea021210143d0466a5e893ff7e7820f0fdb3b14efcc64f9a18cc880e`  
		Last Modified: Wed, 10 Apr 2024 00:54:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:90df49607e0b3c78cfdddb95b1feb82f1c672f715ff60820ce8799410f6fd57c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45158837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb357044fd600d6a4c2ddd8dd5e9a40ce75228853c193030674acd876c34988d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:58:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba028a7caac92f219899bd80fa6f1a5feb00bb36139940defb0418b346547423`  
		Last Modified: Wed, 10 Apr 2024 01:04:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f68e2fb943b11ed49353705a03e10aacbfa2798a63e371096154f467168ca38f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49596491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6034c914c9732225ae6363f7f1d6867937841d2e74a49a5c46bd459d2e6f25c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:40:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7d3c0478e772caba36afc5c3acfbc0145638d0624097319bbbbcc2abf9fd7`  
		Last Modified: Wed, 10 Apr 2024 00:43:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:d151601cdec5b789b06d39fe3b3ca677a390bd9a660671ba033c5971856ed002
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50587458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29edf7b9a36c1d7cfee9c5bbcd5646472d5e918d778ead19c7387131d8d39291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:57:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6c93084f6b3954f71fd45d988bf9435a834cdb32fbbb28f538cad1f41e18ac`  
		Last Modified: Wed, 10 Apr 2024 01:01:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ebd9a1d0ace8e1d3d5da93fe957fd8aee9d2705952ecb43f272badec0ee69dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49567476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0fe8268ca0d6be1d4af80e6f1083f439821d46069e908b9bf6320080e44a12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:09:22 GMT
ADD file:236d3683476bb8b0b7aeab0fd57eb85cfd2718deaba78d6113f3cfd93778c6ae in / 
# Wed, 10 Apr 2024 01:09:28 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:09:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d3071232c2d967757129e1e890a482a53bf14992ca2a151a61f4661b0ac445c`  
		Last Modified: Wed, 10 Apr 2024 01:21:15 GMT  
		Size: 49.6 MB (49567247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e26c7aba58baa1c36a3052f0b1cb1d458c5a886a8a1d3dd5b84dec720f8569`  
		Last Modified: Wed, 10 Apr 2024 01:21:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c690c99b10649875c940751df165e5581011738ff6b044473baf135a195dc9d1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53562702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0d6a3904cb4d5f31d80b1f6210250383d1120a81da42687341ff3e9351b5ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:15 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Wed, 10 Apr 2024 01:26:17 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:26:25 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd61a94b32f4f3f535c69aa42ed952c893f932fa249d941d210454dc845d510`  
		Last Modified: Wed, 10 Apr 2024 01:30:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:2d6d3a97df920181ab747d5a6206071f0131d705d3aafd35438b05f000ac889a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e36ba9cfe8e1203c849ceab28b1d5bdbb2cbfc469e67650b9b2d3519a75afd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:11:40 GMT
ADD file:4b6b256d3328c1d19403b3eb0f375b5d33724b65f790edd27be4adca49c66e4b in / 
# Wed, 10 Apr 2024 01:11:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:13:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:17f5c0a7be3d447b0aca6569b534fabcb69c578072a0cdb81f078fd4872eba70`  
		Last Modified: Wed, 10 Apr 2024 01:48:11 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1581728ee6e202f752fc62677aa908bf03458197aa4f9ea3fa3a75ef7ba9776`  
		Last Modified: Wed, 10 Apr 2024 01:48:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
