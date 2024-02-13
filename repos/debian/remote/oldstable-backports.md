## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:264ac672c0f1b582b86766fb92be4285ea8f4bb53f37406932b0e8dcf377509c
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:5bf8134a48c30eafd8ce9aef9c3dad386477e318674cc4c534b7d4a3ab2f760c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55085071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb412daf210ff537f68bb66ba01e567195ca80955885ea156407e01f7c00a41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:38 GMT
ADD file:12adaa0491b032830c5cc853d99467c3e8c862f7ff6b21d8faf4a42e7e608251 in / 
# Tue, 13 Feb 2024 00:38:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:38:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aa9bf9766217c9580e3ac6604dcc3cd3c02c982063f829281cb602593bf80057`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 55.1 MB (55084849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4482593003fe136e6deedd5e8c3224558e2dae1a3c815009d1b278cae05332be`  
		Last Modified: Tue, 13 Feb 2024 00:44:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5e36e943d1f740be4b3742127c77acfd61075e95978eeb27b49ca42b0d1c6dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52587089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3798cb5ce3520c1fdde0a044f2073cb5fd490a486f73743b2ffaa6d10493b618`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:06 GMT
ADD file:6e6c07c3ba315149b38843b06f144d2842f883f7712dde3bfdfa7309b00dfd09 in / 
# Tue, 13 Feb 2024 01:09:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:09:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54df387d92076dc63bb78e66e5632c3e35c5d9d123dc1444e68a5cd4f07388b6`  
		Last Modified: Tue, 13 Feb 2024 01:14:42 GMT  
		Size: 52.6 MB (52586862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710be30dfd2e518c047376a8ef16b181603d20f949a38af737a31d6899398110`  
		Last Modified: Tue, 13 Feb 2024 01:14:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:42c957eacdec39c492ee52e9a906c1b94a3623de944f3b9c22aaa0e33a07833b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50241918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97bbca56040c24c5f8f81a81d21e28868042940ccb6f366bf4e0d6b08be0dfa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:00 GMT
ADD file:b404d875a3e9708391e275447d08636364ad2852c6b0b8258bc6dae021a64b58 in / 
# Tue, 13 Feb 2024 01:22:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3324cf8629cc8737c3d82f9e83f3848e9de4906818f7c62eaf1131d2642a1eaa`  
		Last Modified: Tue, 13 Feb 2024 01:29:21 GMT  
		Size: 50.2 MB (50241694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19241b3637b8f86bf421711e26c2378cc79d8c510378ad629d051004c80cdbb`  
		Last Modified: Tue, 13 Feb 2024 01:29:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fb03bcb79d097a813263f9a58fa93b18f6e63567d26fc3fb53a70ad15b066345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53721712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03918c1cbd0ab7dea5bea986d6e8418689617b2426274857711a231d08d42edc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:11 GMT
ADD file:32d8fe31dbb8c089d5e7e642bb00599532680798319b1bceb1fd5d2add102a7c in / 
# Tue, 13 Feb 2024 00:42:12 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ac2e38bfa0b9e8c8b65b45dfe6bc8a90b3aedeef76b3f6ab45bf6a654c263986`  
		Last Modified: Tue, 13 Feb 2024 00:47:06 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50289a322f01c01b1312a6c4c56f9e76d8b4c4797fc7f70acda7414156eb339b`  
		Last Modified: Tue, 13 Feb 2024 00:47:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5d0a92363d543f3dedc9cb0ff44100b329b5f0a15e2b6d940b19615d0c81c534
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56058019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74706ab09d993bb940bd089b31a4852b7d9fe9da2d57908cabd959eed6e5dabd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:14 GMT
ADD file:17afc008fedd28ffc8828dfb033f97bae45e220a7c2853f80efe57216d1249f6 in / 
# Tue, 13 Feb 2024 00:40:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:40:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4e9cb2f48c5ff0a03440756bfec0c5fd6a393d86e1a4f2358046abb6f932745`  
		Last Modified: Tue, 13 Feb 2024 00:46:26 GMT  
		Size: 56.1 MB (56057795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22b8cbac2691d2114f7819a18c6d1884d9fbbfc6206289d629ed2d40f4b2569`  
		Last Modified: Tue, 13 Feb 2024 00:46:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:94c32d59b0a420b39f44b69b27960304657df29609044e1acec49a375b587609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad63a5e7b024502c300e4de2b0e4605bc786356366f68bb7c7ec056ac2599027`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:04 GMT
ADD file:5d629b85aff113f4061d5c2082b41bbf522051504f0ec536edfbb3cf289bb29c in / 
# Wed, 31 Jan 2024 22:29:10 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:29:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:010963cca2dc7d83d9ca301dc0979f56fb08edea6b55b03c0501c1e11dc94bf6`  
		Last Modified: Wed, 31 Jan 2024 22:40:30 GMT  
		Size: 53.3 MB (53289095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cd90078adc0d9dbf5d8daa7544f3e5fcd741486d3ec084f309025b2ab33f15`  
		Last Modified: Wed, 31 Jan 2024 22:40:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:96be266d8476879c695be48f123dfc32a5508fe24ea7d5c03ec63ec909610be9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58954730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7597715c63fab4a46caa59a03cb89fdeedb89f5dad319d6fe2684a41446e0cf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:46 GMT
ADD file:f888406849ac951ac8f34017d5f35f82be3f503e464ec03257124ac47ef7be1c in / 
# Tue, 13 Feb 2024 00:39:50 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:39:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2acef893aab15ba3752e927e1ae6e1e3c968222310110696fd7f2af9e455cae4`  
		Last Modified: Tue, 13 Feb 2024 00:45:16 GMT  
		Size: 59.0 MB (58954505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55203d58923bac5c5d000ff1253802762ce9964f70e10319af7c975f5f7f251b`  
		Last Modified: Tue, 13 Feb 2024 00:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:b7e9e4b056666ee72a73045f33a6911869ff2e9748d7a1ea12887aff9a8861a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53319547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2f3a17df888f493b11ac7257d8f82c8ba322c5c1521e3d07baa0d6ebccb30a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:07:28 GMT
ADD file:29b4d794895abc9141edc10e7fb6afd82c9c6037d8f6189898a4c74107dbcbe2 in / 
# Tue, 13 Feb 2024 01:07:31 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:08:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0e9f1641c29b12fe83e157c576733382a1e4f21a81c23bceab35b7be1c0e3292`  
		Last Modified: Tue, 13 Feb 2024 01:31:06 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276530db4f2e3b79d46583934b88d8e156c306da145c64abcfb2a838d6dad4b4`  
		Last Modified: Tue, 13 Feb 2024 01:31:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
