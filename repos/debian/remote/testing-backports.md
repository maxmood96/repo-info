## `debian:testing-backports`

```console
$ docker pull debian@sha256:2dc09ebf0caef65a9f4e44e64aac73f1a2e5369d1341f80039ba0a9298307ec9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:9ea7b9fc5063d71caedda826f6e60f7a7565f816ffe0547463b20826e9cc2dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48836724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809c98d0bca21fba1ad9dc8d23541e7e8996a11e34c6542989e1684d8fd2e67b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:16:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5abf542d95a9328e19a36e1d742dd98dd9f67b38be29da7b849a1c9e274c1583`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 48.8 MB (48836502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff3aba4384b3fb3c1d93c843db8faac3282704ebfecf99b103acf6f736adf72`  
		Last Modified: Tue, 13 Jan 2026 01:16:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3bcb3055b077bf1ce443200c5c8f7260f46eb1679dc816fd32db04537e0e4fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4e0617ef85f1658f10ba74d479c3a58196f9817551563b36c142031e39c5e`

```dockerfile
```

-	Layers:
	-	`sha256:086ced1680ef210abc92b80cd78e3171b080de1816707a4ffc9f58881555c7d0`  
		Last Modified: Tue, 13 Jan 2026 04:27:15 GMT  
		Size: 3.1 MB (3142043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561d57d40462706d4167f006c1401da5e8d145e2c83ed520d2e0ab86da1f6990`  
		Last Modified: Tue, 13 Jan 2026 04:27:16 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:81ec21bcef14f85f65a6782d88d4f858012f29c459573a46a8ea8cabecf7f69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45128725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d802ffbc5ed69dda32f29e495606b400cac3777439c6fbfeaf61f65ee146d2ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:18:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b52b83a8ae7e06dc9628b08b5ba1e89d1671fe275e5a1dad70de57feeb453db8`  
		Last Modified: Tue, 13 Jan 2026 00:42:10 GMT  
		Size: 45.1 MB (45128503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611bb61db6d32fa947523e363731f4e7d623b0f38fc5a9376b7c2bcdc08c9402`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fbda5f7bd486aa698cfb70c8f82221ea1d8eb36ed7339ff24e898ee8ea49c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86619d6f6192b1b5bc720413f9220dc2affa0f1003e9ec0fb23191e583d2e0`

```dockerfile
```

-	Layers:
	-	`sha256:190d7137c024b8565aad11d9c2f88f66790dfd366da222466d59c890f3ceaf0c`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 3.1 MB (3143411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62f50fc397c07f05ff45b376fd6fbec8c43573004c56945a8be12d7dd7ffbf8`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4c05a128315a5a9141e0282f97c953a86a88a280a8511807915562c9b5462446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48821035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5abde4a2d47455dbb45cc5d309b14de677ce8749a4b0c85667e91f9c466884`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:17:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7bff1ad60177e8dd221d8df5866b0e7967fbd97f4eb69a5eb672bd24b7ffc9ba`  
		Last Modified: Tue, 13 Jan 2026 00:43:11 GMT  
		Size: 48.8 MB (48820814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67630b0a3b96fe8dfd739f8cd78d925902da72bce8f2906e2fb798ac73919517`  
		Last Modified: Tue, 13 Jan 2026 01:17:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90a776a0b5876c0e7606bdd7f3b5f8000faf37f7ea8495782253ec1bf9cd7402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1697a641199649088b57b920c8d281e19dee86a4b6cced0dd35118910eaa179e`

```dockerfile
```

-	Layers:
	-	`sha256:824223458fdcd00e5c170d9c3c00420d3dab9b36935af9b8f95de63ba4e9cae5`  
		Last Modified: Tue, 13 Jan 2026 01:17:18 GMT  
		Size: 3.1 MB (3142884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840a8f67ca1497379e58eb2b685fe129a77d8b7bee820a3bd1d9db6187c73e83`  
		Last Modified: Tue, 13 Jan 2026 04:27:27 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:ce5b3ebaa8699fb70055ab45f87c3e0ecba708e385985027f6f90708b2f41dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150c3736ad0b88acee9752ecf5c3210fdc84a1a7761ea5a5fe8e0d8fdd698fba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:18:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:65a17761f67102b9b31e6ba09bea12e37d10922372c16ce1a4f483d5e6df64aa`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 49.9 MB (49944551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b62f140ed240e1b26a66dba73ea74702517cdaaa50f99df712aa5a8b443053a`  
		Last Modified: Tue, 13 Jan 2026 01:18:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e3f02290719b157b22c2b75fc179913e611f50c550d9b76113bde2f176bdf55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb5911b0e7095abbf588191e27db52c07ad498a7b04afea54a08b23852b3102`

```dockerfile
```

-	Layers:
	-	`sha256:f9acb89edd38f81458e28afa75ef5952406f801b93daf56d5d80abc2845dba4e`  
		Last Modified: Tue, 13 Jan 2026 04:27:31 GMT  
		Size: 3.1 MB (3139247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0b84d88df194e9609ff867d18548a1b463acd01204b4c67e01c64d829ace4d`  
		Last Modified: Tue, 13 Jan 2026 04:27:32 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:91416e59bc28d943d21f042ce8351a2ad3a3e4586ef38cf689564f6a5f98eda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53516410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f935d4fb857a4031be1e3e392fce7764aad57ca290c408ced36766e7c9dc6f78`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:16:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3c09db137a92dd478d776e54d49034b249ad15299a714fc28f5e13f7c59c6f6e`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 53.5 MB (53516189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1aadd291b1e87c27c8856341d22e4c9df5508c1bd49e0c4db829f7e08d1b8`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a315eac45d644b16183021c28783e354c13837cf2d48689ef9d40a50323f0bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad782400e48aa79c5046486e2238157b905d5ae11b34e6328389ffe99b30d45c`

```dockerfile
```

-	Layers:
	-	`sha256:5228e60889c33395193a9ec2af007915421b05444a33d2d76a40111721119ff5`  
		Last Modified: Tue, 13 Jan 2026 01:16:26 GMT  
		Size: 3.1 MB (3145546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736bcb182c37f9e24339056fe539bb0625137b506a4744606b898823e8ff93bc`  
		Last Modified: Tue, 13 Jan 2026 04:27:37 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:fb3f274ed7839886023de45dc2e02c7fdbaef052f60338203d6fca695c8392a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46854688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868dd2984733b77251c787ed941b6b31341ab68d2280c7358f98a18d6fea2cee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1768176000'
# Wed, 14 Jan 2026 04:07:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:91e82f1d58406699b930594305527c53618f59da57e5326a595907e3493b82f0`  
		Last Modified: Tue, 13 Jan 2026 01:02:59 GMT  
		Size: 46.9 MB (46854468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895e2f7e7862637d229f9598e10597a1261ad3a4fbd1b8e34660be054d5f706b`  
		Last Modified: Wed, 14 Jan 2026 04:08:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eeca3de25934e33c48334a219c81a6ed7497c2dbf5dee16f46cf2c5428f39e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c940681b5da64f7be4126ba2ff8167e8ceb76e21df52d370d7be2311bc6486`

```dockerfile
```

-	Layers:
	-	`sha256:eb8e91d8af3f130cba6082e1c93e4347b17a4220046c6896cc6a97f6d8d50dc7`  
		Last Modified: Wed, 14 Jan 2026 07:24:53 GMT  
		Size: 3.1 MB (3133541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7710d291674518d0f94515c05703921690d4d88554ecc3e1ae239f4a7b92f9`  
		Last Modified: Wed, 14 Jan 2026 07:24:54 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:6cf2ced03746db9e96d7793998b49d5fe4678deae7490813e3eaea2a60a83999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebc02cb8263ff133566e0d72209a4b86278d8a487261b9a959eda9841fa6a62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:62ffa4c0309d07ab05b7709095497112179f2c729363c4d63136ece116e95e0d`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 48.4 MB (48389301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671b25e4372e0c1db6dcdc3eb6940c6670c4a13f9c70326ef53118c0e6a51648`  
		Last Modified: Tue, 13 Jan 2026 01:15:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6324a7b6677162b8d724b21c7fda4d3709e939cc9cf78b07292c1787e0d21725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3255fd8887be3b490cbbd18fd4c7bf06b940a49f58b075c17587317e69d8bb3`

```dockerfile
```

-	Layers:
	-	`sha256:350f5dd559361d224f775506abfc23b8e2a5ff738f6ff77fbbd414ac7f8759a6`  
		Last Modified: Tue, 13 Jan 2026 01:15:23 GMT  
		Size: 3.1 MB (3143492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded9967ef86943bea0581e5702693b8a89218dceb97eeefe3932a944cc616748`  
		Last Modified: Tue, 13 Jan 2026 04:27:46 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json
