## `debian:stable-backports`

```console
$ docker pull debian@sha256:e806145316b8d474ffdce7c14c81112add629d9340a0e6b5a933c8df99bbf502
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
$ docker pull debian@sha256:35981c8993dd9db40ed3becfddb3b6bc4d7d3b9832337368e1cc274a7b289844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40ae3c3a98424be7f81ffd5cc7acc71a4f3b5e1d5185afa3d0690abae6b1a46`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:35 GMT
ADD file:d55795d0db42b960cb26a71300c9e09e21a8bd517d9d456b139e107bd11a559f in / 
# Wed, 20 Sep 2023 04:57:36 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:57:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f479ab1f1d7313a83d1f2617085c8111323342da5f3b6114f4834c955a686a85`  
		Last Modified: Wed, 20 Sep 2023 05:03:41 GMT  
		Size: 49.6 MB (49557606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bf42fb9eb120c785d3743f767ea1b955fdbfba3679127e6c9310aa6e68df5a`  
		Last Modified: Wed, 20 Sep 2023 05:03:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c1f07d71fbe30eee6f9815354f333faecebae2625087b17abf84f4381cea1265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47415215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d52b1365c190c01e79023eaea411c355565736a77d1c53b6df7ae5bacc3534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:51:25 GMT
ADD file:53ceb96e5672e219aca6daea64bd7cfac4dd9ef4811d93e8f1425341c0b5143c in / 
# Wed, 20 Sep 2023 00:51:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:51:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1360ba697847ba50544626e2fdf28d6189f0906348cc31ecb1f8ae807f15a790`  
		Last Modified: Wed, 20 Sep 2023 00:57:23 GMT  
		Size: 47.4 MB (47414993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82384d58a25e38f5b3c0107a834b251df6167c28353743617ced7d51385a58a6`  
		Last Modified: Wed, 20 Sep 2023 00:57:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:924b03b628aa99b69679e267b5477d8655e95cd607c10712384a7ed65e6df85c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef93e1f62f6caabc086a2a8d6ec4723364c58b7259540778e539328e97bba9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:56 GMT
ADD file:f36210c9b1bb49eab25ac2301e39accfe23fd78238d74e1729121c65e2a323e4 in / 
# Wed, 20 Sep 2023 04:58:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:58:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d65e795667b305c061b0d69f16ed2540c215d574af74080fbf9d8ef3e16d513`  
		Last Modified: Wed, 20 Sep 2023 05:04:33 GMT  
		Size: 45.2 MB (45232556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e24a31bbe86f766a719c73acb9125b61fbc575410b78e6d588e0bebe8daf746`  
		Last Modified: Wed, 20 Sep 2023 05:04:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e00dfd4bc9a982a9d068e46752fa6badfac91e0c6a3c10c22ecbb6710137157c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49592067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f23ad459a1e7b4a6283836bc6f365927196217b89e5e58b465ad21ea0fdea22`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:29 GMT
ADD file:ec644050dc5561e64384a4e0d183df970aaeac0750f1f762ffe29b7915295eeb in / 
# Wed, 20 Sep 2023 02:45:30 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:45:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3dcf5c113a64725cb576d2f4e678aa926bd6ae3c3f413cd83e23503819fa61c`  
		Last Modified: Wed, 20 Sep 2023 02:50:30 GMT  
		Size: 49.6 MB (49591844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945e730b58d50b3bf97b17885f7a47077182ab5cf6bfc4698ae0f3dbf1f3d73`  
		Last Modified: Wed, 20 Sep 2023 02:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:24347bd56442601a884eaf625cbdfe0fb4ca25e298ae4e0c776e395434f7766a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50569192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd2fc574aebdd8c4223b3ab84a09b64b3005ae3136a468e910d6cb8487f9eb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:55 GMT
ADD file:a4f2fa3e98a8185764341fd63ac3591952b23182853ddd2ebf84ca98a3169ebf in / 
# Wed, 20 Sep 2023 00:43:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:43:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4737eadb65c1f5f944f365a8626d47a469de86152a9f43f1178dd43ee1507fc`  
		Last Modified: Wed, 20 Sep 2023 00:50:38 GMT  
		Size: 50.6 MB (50568969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461c1d5dda8eb5ef020bf7a9130f1f9080afd3804c54012f114d2c13e5028390`  
		Last Modified: Wed, 20 Sep 2023 00:50:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a3426cc4606e0219a3da4b99a404fb4922136e8db8cca8180a8787a1ae401626
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c60764dd42ae95c06779e569a8a6758561da018746eec360c96f141e385de5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:14:12 GMT
ADD file:0f58f69aea93341db2a8b649d150e02eaa4a5504313cad47a7363c84670830a0 in / 
# Wed, 20 Sep 2023 03:14:17 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 03:14:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54259548d3370f255becb131e7aa6e1bce367a442b76dc799daa0fa7ea1de9d5`  
		Last Modified: Wed, 20 Sep 2023 03:25:34 GMT  
		Size: 49.5 MB (49542379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c762ca16d6df56e4c27a9e3151d994b3a7b1f34ed12d3b9168812b9f3cf7943`  
		Last Modified: Wed, 20 Sep 2023 03:25:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:443f20dfb1134d6aec7cd06b5eee0f4a88b1b416f81a444d958153dcf8f7593f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53544942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41b19d4ca37b7d0f191d92180b9eb864661a66ecd4986c004cf9ad89efabf5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 07:55:13 GMT
ADD file:3c90ee7c1a136aa90ff4e9799fa5bd0286ec776adc8d88db66c0646d0d4f24c4 in / 
# Wed, 20 Sep 2023 07:55:15 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:55:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3512a4ceebf002237dc06e3af8fae2b9e6f0df346fe116d9b2000f5012b5cf1e`  
		Last Modified: Wed, 20 Sep 2023 08:52:34 GMT  
		Size: 53.5 MB (53544717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10a8d3f23c46fc26dc4490221457ce83fd304ec20e0310e523b25a3783fc54c`  
		Last Modified: Wed, 20 Sep 2023 08:52:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:01f4f6a3bb2cfb16ede3bee9d56b882dc827179c797f33fc18932253ef9737c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47921992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8945029783e1c3c586fbaf15ba0031c4ce00050a6e732300875ecfd8f3d66de5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:56:19 GMT
ADD file:fc6cba255c7e2ca2b3c811950c43cb205c3af8556fa9d269cc5d59271bc28bc5 in / 
# Wed, 20 Sep 2023 02:56:27 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:56:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9c4c8e345cd7d3d64eaa70c6bf00a5d3a9abe22d4184e1384d995a1d2ad16547`  
		Last Modified: Wed, 20 Sep 2023 03:01:25 GMT  
		Size: 47.9 MB (47921770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4b588b0f9f18a8d8fafaa0c7a42b46c78ada64f56718de994ca84886b98bb6`  
		Last Modified: Wed, 20 Sep 2023 03:01:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
