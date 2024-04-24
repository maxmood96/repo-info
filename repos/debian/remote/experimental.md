## `debian:experimental`

```console
$ docker pull debian@sha256:1341cb6172e9173f23cb931158f60d1f7dc5d6cc70605a0c23bd148311859691
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:ff30bef843ce6de92a79e1f9e667f942d5c6e7fb1ee548220c02c85fee9a3968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51736117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a3149af36460e1c22e7c6b337e1146321152c185f19c3d7f9127693efc45c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:59 GMT
ADD file:103cdf14b755256657dd553a841386eda681d37329fc3828a7d2c0307fb6bfa8 in / 
# Wed, 10 Apr 2024 01:53:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:54:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b3fc1425b300907225c5c0b4d59a5611b9b18be92f89781c5c26cacdbba24201`  
		Last Modified: Wed, 10 Apr 2024 02:00:29 GMT  
		Size: 51.7 MB (51735896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aafbfd7d08607e148a550b7e109421bcf3000496756e80207f5a7bbebcdca95`  
		Last Modified: Wed, 10 Apr 2024 02:00:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:1e7c440ef03f4ed386ce39a0d78499cf580b76028d62dc497a4849ce2c310bc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4245b1c64cc34d45caf64cdf61db9d22c8ccbfe1212c1f8db65f23d997ada04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:52:35 GMT
ADD file:4a9a5b60f4b0feab990acdb3d3ec5db34081842dc5daae1661318093af948c84 in / 
# Wed, 10 Apr 2024 00:52:36 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:52:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:05931d6d04be6f738b1c2bcef92c2a5f4e0ff74f0547a35b66b31ada25c2ff81`  
		Last Modified: Wed, 10 Apr 2024 00:59:01 GMT  
		Size: 48.9 MB (48901907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127cb4586705819d08a7576f224e167688a06628986369f5051dcd07af72f0`  
		Last Modified: Wed, 10 Apr 2024 00:59:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:cdc7ed24b470d8ae090b5ac58b9421d0a4b6398ce4c3c06fbd6bfe14ae3764cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46488440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703fd8dc2ac65ac50b6666bc2ac958373f865e1eaa2bab02265e8ce42b770c5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:02:26 GMT
ADD file:6f0a8c377fde9fb715f33a10e7021e5fce759f4c0971b9890c1042895d7609ac in / 
# Wed, 10 Apr 2024 01:02:27 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:02:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e1c0af1983206d47edf0b761a062a04b143c0a3a84214c928924d91004fc4967`  
		Last Modified: Wed, 10 Apr 2024 01:09:51 GMT  
		Size: 46.5 MB (46488217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b30997f754b53c281bb92f0aff6b98277a215b977ac324b9972215253df916`  
		Last Modified: Wed, 10 Apr 2024 01:10:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:179c28456f4db0a00b4838d5c0f58c62cba312925ffc6891c510b966340e2e5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52137228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904281b7eb9d308f5bee265e4db36646714dce931a0749493b11588a865e91ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:42:29 GMT
ADD file:e6fe5f0b8c3528802b709367c8aac4992118997544ce7ea9830bd785999dfd1a in / 
# Wed, 10 Apr 2024 00:42:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:42:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9426fab488e6a861850915dc20ebf0dd02f0a78d49b732b81a99f89fd93caa73`  
		Last Modified: Wed, 10 Apr 2024 00:48:48 GMT  
		Size: 52.1 MB (52137008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6195eb4f8878be1c04e0a2fc641dfcdbe5d8cad5c469d2e0d880d90444bbfe0f`  
		Last Modified: Wed, 10 Apr 2024 00:49:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:3e7faf06b15e11bc1b779026a48638843639c2af85f482567026a52860e96bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52545506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d93a9691e7bdfc882bfd4d24f977aaecfe45cf99623b2ee99f241f69fcf327f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:24 GMT
ADD file:1af1b2fdd22c6c9c401d825f279cb7bad31b4dd82b7a6406fe389afdc8df479d in / 
# Wed, 10 Apr 2024 01:00:25 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:00:37 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a81460d22c87e240573251ffb01a1f08d73320c4eeaf4ee018bddf66f594fb9c`  
		Last Modified: Wed, 10 Apr 2024 01:07:57 GMT  
		Size: 52.5 MB (52545284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2670738c3ce1fa1a4d9b1eb6d2b001d420e36b4257e1dbbf028b0f0fc7fe69`  
		Last Modified: Wed, 10 Apr 2024 01:08:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:5cc792b17f67ec9562c00114c4ca8a19418708453391f558bb941972ec152201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50814854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b12d1d1f1ccf6a602c1c49c787822f973afde1963a14870651750fd0344fd58`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:18:52 GMT
ADD file:c1af6706735aaddcb2b2b4a6acb87702877ded463d000f839968d38b8f8c1390 in / 
# Wed, 10 Apr 2024 01:18:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:19:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8381609806aa03cccf174815f59569a30dba532399d669fb8aa1c56aa9931147`  
		Last Modified: Wed, 10 Apr 2024 01:30:24 GMT  
		Size: 50.8 MB (50814631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5e4422c6b6b2b1b3199e8e6519217b4dd4b6f53f916213b4c2a0ac6c7ed24`  
		Last Modified: Wed, 10 Apr 2024 01:31:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:55d77edf40f9333ca2cf525744d0fb67d587928520f35db662676304d070dcfc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55558959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632ba014d0eeea17b817b70507fe5a95630919be0485b71e1b8c1bdc0fa92316`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:29:23 GMT
ADD file:c43544b5bdb8d636396318da7f46d2ac3baf4a00858bdfd24ee20dee9a085999 in / 
# Wed, 10 Apr 2024 01:29:26 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:29:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b55e54510048bfaa02833e7873c460e85421319a954ddec6ba39c4a8db4ade6a`  
		Last Modified: Wed, 10 Apr 2024 01:35:32 GMT  
		Size: 55.6 MB (55558739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf79ece49c26b53a0cb520481a224c6b3c6e1453063bde5456953f89366e9c18`  
		Last Modified: Wed, 10 Apr 2024 01:35:57 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:e45dd5de4890a0ad3a4b9a414b322ff663d137f229ef8793bb8d8d2715d1e015
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50665633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a40fc9c6c0ac1d95b8bccfaa6cce21595290f4646d072982e50d5286c41588`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:10:43 GMT
ADD file:a95faf1f554ae0b300491cecf4c6673ac4513e69d5a04e655b5889bd1c72bd65 in / 
# Wed, 24 Apr 2024 03:10:45 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:11:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aa8b4e50fe262518d117b4f920dcd7ede0214f4a5910bd41e86ba9e6b178aef4`  
		Last Modified: Wed, 24 Apr 2024 03:13:45 GMT  
		Size: 50.7 MB (50665410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704c7c754175ddd831b2168dbb146fde3bf7413c2d95fd24473ebd85a0989740`  
		Last Modified: Wed, 24 Apr 2024 03:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:36fbe8ebae7c364cef320db35b3edff0650d6d7ac6aa02bca6a07cdfd9652aea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51141630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597ebf9bbd3b902c2271e35e3cdab146f69c7ff5778f4e137bea5b2b47033e93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:42:22 GMT
ADD file:9de273a9cac02a91aa5194ebcf6e7af04310e5088a195bbca86a13caa2b5c506 in / 
# Wed, 10 Apr 2024 01:42:24 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:44:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:36df309cfdf175cd9ee1452424bf2b03258181ad40da42d7e9a34da8f7c3acaf`  
		Last Modified: Wed, 10 Apr 2024 01:51:27 GMT  
		Size: 51.1 MB (51141411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b9b64c9bb206b838d791f384f3192e3afd53d63554cee9d724c3972ebe7ca`  
		Last Modified: Wed, 10 Apr 2024 01:51:43 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
