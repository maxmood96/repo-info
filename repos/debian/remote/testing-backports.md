## `debian:testing-backports`

```console
$ docker pull debian@sha256:b8475abc53fd9eabdefe6e12ebb516da78514d4fa4cb8e1f05d9e52fc2aee093
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
$ docker pull debian@sha256:24863766cef48c18489c98be9db1bc02801ec50fe31ed382a4b782416f440b1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53178273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bb593e586f7049641d239ed77f5170d8430420300e0ba46f3403d8c5f54dca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:11 GMT
ADD file:d124f58a75824fb48cc5bc8f7954157ace87dcf80be8ba17fd0bb3fac8f6d19a in / 
# Fri, 27 Sep 2024 04:31:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:31:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:082d57a12cea884a5f3c544769a8e5aa73570907b945a48991f31218efa6a3af`  
		Last Modified: Fri, 27 Sep 2024 04:35:32 GMT  
		Size: 53.2 MB (53178053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e425bf69df7d586d59faa82a4641bbef6925cfd466ba97a0938e710b596995d`  
		Last Modified: Fri, 27 Sep 2024 04:35:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:df1e41d3e1e8d0a3c429e01c22c40e16863c5a1f15eb0bb8578bcf798ac6fb40
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c1430e46e101ebb58394a9dbeda135d162796d6ed4e16061ae74c42ab4a510`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:02 GMT
ADD file:0993a88b458abaa02b2e2b447232a8aec6e642b1cac6cc3a6dc1baca59502d56 in / 
# Fri, 27 Sep 2024 03:20:04 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:20:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:abb159cf32a8d031f4b0244e4192b20af050e428423362ee8826a4906d7eec5e`  
		Last Modified: Fri, 27 Sep 2024 03:22:59 GMT  
		Size: 50.1 MB (50140667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e4867a29d15c784902b32e652dfedd3e49b161e08cbeaaa228c3c52b06bc5a`  
		Last Modified: Fri, 27 Sep 2024 03:23:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:35bc2f5fc9349a2118e511bf6e683375c542d102d4f5131a5559646983a87fb2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47634156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95dfc69e370c0533767262e4da0013792647db83355fa1c793054cac0b31660`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:21 GMT
ADD file:fb5e39f7f5bcfbaa21f64fd97ca1564921b5d0673fe330a8834c706152a09859 in / 
# Fri, 27 Sep 2024 05:15:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e46465b055aa50600d1bdffbdb586bb40e82873206be9d67794a93d24d546e91`  
		Last Modified: Fri, 27 Sep 2024 05:19:34 GMT  
		Size: 47.6 MB (47633937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1bfd82f21bd8b8e3075adbbcb04fc275f8385136674ed2cd965a7a81f5c853`  
		Last Modified: Fri, 27 Sep 2024 05:19:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:66d37c7ac51aabb793d91b58f502102244e76b411ddeb2f0ca1047bd4d7ea172
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53616810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d31adecd0c1a4c1104cb37fa19adf1409e2fa357c374701b15e0009d0adc91`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:21 GMT
ADD file:dfa41c5a8e1c4511359423b532cb30507d2ec0cb9ef2412143a4d4a2752d2d0a in / 
# Fri, 27 Sep 2024 04:39:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:39:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be8a7f4a2cec45419ae4d29243820f77c134b84630752f45d42a7725f62db14f`  
		Last Modified: Fri, 27 Sep 2024 04:43:03 GMT  
		Size: 53.6 MB (53616589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756750d78fcb3a79314c4780c39070bf6456c97cb5130a432771413f3e72e65b`  
		Last Modified: Fri, 27 Sep 2024 04:43:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:532be043a84379d79cfb9798da3b0f6ad7937f6705890950ec381a68dc840dcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54060186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df567585677aae22cae8fdb9f08ce0199f3e89153f01553023dda9fd5a21934`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:24:42 GMT
ADD file:0b7112062e9051a8709edbd581316ab7a47f0228750e5ea3b688528caea7ad68 in / 
# Fri, 27 Sep 2024 07:24:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:24:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3f958915033c0bdc56731d6d202936877348e562bc4aafc42a19ab51d734caf3`  
		Last Modified: Fri, 27 Sep 2024 07:29:53 GMT  
		Size: 54.1 MB (54059966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3912419a5bddc7d9fe7b5bdea1984bad2a503eea0f10bf03a19faf0222b61f98`  
		Last Modified: Fri, 27 Sep 2024 07:30:01 GMT  
		Size: 220.0 B  
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
$ docker pull debian@sha256:9fa1498dfa020fd692f0a64918afd155409ffd79b3b77b90130e6b9636769922
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57100602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ffd50454b812c89e7967f9ffd6972a165ada878ee0783bd4911766448b45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:08 GMT
ADD file:1cabb289a72ffeb44fe38a5ebdb31c8f6a7bb3e5fd5c46b1b4132b34443c5811 in / 
# Fri, 27 Sep 2024 05:34:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:34:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4fe1b2916866944b77c438d068d2b8fa4c195832fc93b9c0068bfa8310f21499`  
		Last Modified: Fri, 27 Sep 2024 05:37:42 GMT  
		Size: 57.1 MB (57100382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91188ac5324eccf5442409c38a65cb46bdb9195da0420988aa015240a3ecdaa8`  
		Last Modified: Fri, 27 Sep 2024 05:37:55 GMT  
		Size: 220.0 B  
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
$ docker pull debian@sha256:8331483eca7de5fd6d73794602c09fbdcfefe0af5a1226580dcc5b04168fe52a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52771292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beecb6c10dd580d8ac05abe754c4a4ecd9b2c759049adcad5b325cabbb03503`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:44:52 GMT
ADD file:3e39c625eaf60953d8cee79d51e2111b241d054227598d815a080b9fe676b690 in / 
# Fri, 27 Sep 2024 02:44:54 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:45:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6254903b6edc85d1dc106a3e9025a77bf951ee477df6401427b61d5e2f6ccc3a`  
		Last Modified: Fri, 27 Sep 2024 02:48:24 GMT  
		Size: 52.8 MB (52771071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab3693a9ca66aca483f81143a7c9138f7ae1dcfa75396ab3391aa67796da15a`  
		Last Modified: Fri, 27 Sep 2024 02:48:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
