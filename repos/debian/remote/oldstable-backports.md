## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:057a5f6818145ffced9a3b267f463919d77bd7d42ea4684cbbe74c38d982c691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3a11906dc02aca0eb0d6d9b05c4a1256d9313aef7c678ced21bcca8414d2ed06
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55080862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2023418993ed777a978238914ca7bb5b09e11953f785b12082e3685cc4188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:01 GMT
ADD file:8f3ee56a8d465cbde69dc2488a717f0af92d3576ba504baa9ecf4a44bceb0ba2 in / 
# Thu, 17 Oct 2024 00:21:01 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:21:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45b81c812f9140c27b65b7cef4ac4bef82357b8e87f35328ec1acc9d529a2f30`  
		Last Modified: Thu, 17 Oct 2024 00:24:52 GMT  
		Size: 55.1 MB (55080638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a28dc9a4dd00b97c702291ee98f32f6c5173b27fbb439382ecf4dffcddfbdb`  
		Last Modified: Thu, 17 Oct 2024 00:25:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:738a035d128874f669c1cc8c96f95502b6b0b38ed14b3ed4d144d96bd9c78657
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50241835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b204f8bbf297a7e5d210b7dd0417d64e160652cbf6e75941646591b6b39ca19a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:56 GMT
ADD file:0cf97f2a5d0af563869c26f0ffce862a80841a7c628ed7e25ac238cff0cb2e26 in / 
# Thu, 17 Oct 2024 03:03:57 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:04:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:83f1e01f9fdc16b785f293ecb3b08dd0e8f4acdd2809f47ebc6a9312c1925868`  
		Last Modified: Thu, 17 Oct 2024 03:08:29 GMT  
		Size: 50.2 MB (50241612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a3d60428ce6b739beeabab963ab247e9ffe46ef66997c468fd2147b395fa7d`  
		Last Modified: Thu, 17 Oct 2024 03:08:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:97cd655c459db97f45b1368707602f9b7bcb04a5b0d9c7871bb133101527911e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53735113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8a91604df01ac3891d6f4218f65ea86acc0babfe444e01184b86479803a00d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:20 GMT
ADD file:00a1ea325073eeb22860c205faeb9333d3079ad96e3ff7c709473cd8188b2bf9 in / 
# Thu, 17 Oct 2024 01:12:21 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:12:24 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ece85efa95bbf1cb2de5fd546338023aa09d7ec6b82338518b3e7755914a8c7a`  
		Last Modified: Thu, 17 Oct 2024 01:15:29 GMT  
		Size: 53.7 MB (53734887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5084d2b065a8597d02b0263d8233f7808da28e48fedd2bcf98656becc96f99b`  
		Last Modified: Thu, 17 Oct 2024 01:15:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:041f88daf094deb20486c6ea6260d208f49489f3cdc50614dbecfc1bc546d82d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56078045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4f7d6c6f2aa8ccc628c2c034e5a2224cf080a4c6be74a09946ef1c390b35b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:30 GMT
ADD file:55edb81e795f579b3a7e08f1359e6196988284f303649d34491783a36cebbba6 in / 
# Thu, 17 Oct 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:39:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fef51032d42b4132aebafad5bbaea13516d3a06fc7af7490027b0d30eabb39e6`  
		Last Modified: Thu, 17 Oct 2024 00:43:35 GMT  
		Size: 56.1 MB (56077821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d705e81f52e8782208ebce1abf3934bbb6754451274852a873f89bbc60c4082`  
		Last Modified: Thu, 17 Oct 2024 00:43:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
