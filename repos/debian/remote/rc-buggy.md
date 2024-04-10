## `debian:rc-buggy`

```console
$ docker pull debian@sha256:a3966fde63e33108fe3dba1bdac54d4890b9e4470a5faaf33dc1dc0a3e4580e1
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
$ docker pull debian@sha256:9628bae7b42350b3d558f0a7d41643956fcbcf96adbcfb2d529dac03d0ce6de9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51736109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f7227596e0ff93c9e01720ef85b63efbfbbe01887c7d59fa8b9ebf5214fffd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:30 GMT
ADD file:7fec587617b78a81cacf7bfcdeac3b9e90b4135c4c242e80b5ea34f57d221168 in / 
# Wed, 10 Apr 2024 01:52:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:54:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9c331a6d36afda0d91938277ed86b71e85bfb5904bb0efa434e13d0991817c34`  
		Last Modified: Wed, 10 Apr 2024 01:58:18 GMT  
		Size: 51.7 MB (51735884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d077312cb7ba4c27f993aff2379dacb506bc1ae3e43628d9981abb013dc383`  
		Last Modified: Wed, 10 Apr 2024 02:00:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:927a37b82a8ba8508f25e9fcc9fa5d1b9ed37b8513644daf434be9344d7aa953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc0bf6d031902c8b8dfa405ae010c5cdd0eefa6dcc9efa02631d2b313eb46f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:50:32 GMT
ADD file:4a9afbefe640815ceed7c04b5539d7c65f79afb1c50420641fb90ea84d9456ee in / 
# Wed, 10 Apr 2024 00:50:33 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:52:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:435c81b262aa45b615a98b5b08f6124900f0a2f8c1b016424864ba2f1ed5bea0`  
		Last Modified: Wed, 10 Apr 2024 00:56:32 GMT  
		Size: 48.9 MB (48901894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8aebcccba5679a7fc2346d7f2a4fc10d4125bcf82130959b04b3cd48971d5b5`  
		Last Modified: Wed, 10 Apr 2024 00:59:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:8adf63a9ec0e7523aa5930e35c38af2a30fe7083f20765b46881c85dfc0cc53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46488438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03949c4110701dce58b22d605843fccbc3756ac279d5eb4b341fbc15f9cd8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:33 GMT
ADD file:b651a9e79740799ad0cf7f17474e58eefdc73e4611a56f8f166422f38c62fa53 in / 
# Wed, 10 Apr 2024 01:00:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:02:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3bb537406eccf44a062d659169f21696e8c3000511c07deaf7acadb77364db29`  
		Last Modified: Wed, 10 Apr 2024 01:07:36 GMT  
		Size: 46.5 MB (46488213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d132ee4ed55f117d06e08ca443f5d5d62264d59cb082c36308fdb9a2d92c0d`  
		Last Modified: Wed, 10 Apr 2024 01:10:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c16c2e0f3ab4e6df907769ffa09d6c553b1b42b125801f2f5ec126a7a7dfe370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52137223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb193cf6c65a4e588670f3f578faf750e009eda47e77c1d998f67b5bd681e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:42:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd3ce6f097b077224c8c325f058c7e0b3df43a515a88a90d047ce33a97397f2`  
		Last Modified: Wed, 10 Apr 2024 00:49:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:3f14b4e4db8e27ebd1084f80317d3194ada860470b0cb0f9dd58459565456b23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52545522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af872a13df07aa7d4be8623e28b97dd932a2830dc9a61b74fbe321460750175`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:00:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5db42d7a9b175c8369b50f1c5c21143a32f63abf95c80593ab8970afbe447d`  
		Last Modified: Wed, 10 Apr 2024 01:08:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:cdf0f9cac06ae9d15ba7acd49272425ca9cd52df39bc8bc7b06009ad25543533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50814857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77de6ed01b4ffc03b47e8b484d9484db1a53b504252585c65d26c0f860cab9e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:13:28 GMT
ADD file:6c115df8d41d96a6520599c767a96584736ea315fb4abba16fba15c638d24338 in / 
# Wed, 10 Apr 2024 01:13:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:19:53 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6b337f2d29cf3d5aea69862db4f9452dc2c952aad643e9b732cd86bf32e8ec80`  
		Last Modified: Wed, 10 Apr 2024 01:25:24 GMT  
		Size: 50.8 MB (50814629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300664a2c1e90774f85dc36bc7dd38799a1476848380973c35c39217bfda3c60`  
		Last Modified: Wed, 10 Apr 2024 01:31:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:ad05a00433a2f4961479ee9e3960615eb0f2826366d5ced8f803f4a7b7ab41ec
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55558976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a059392268542d08d3380a3734cc7d849944db645d6a50fc499115161848b4df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:40 GMT
ADD file:b4d76c20a1ef31eb6916914baa486e040481cfc4a1f2464b19f7a54de07a7414 in / 
# Wed, 10 Apr 2024 01:27:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:29:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:149ef7b943fcf6c968df7da67a0cab193a9c8b879654558231f5a04b02ace929`  
		Last Modified: Wed, 10 Apr 2024 01:33:03 GMT  
		Size: 55.6 MB (55558752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcca74071bdd44e467b65d462e62caf0728a1ea3b8bf68e647f8f63846290d4`  
		Last Modified: Wed, 10 Apr 2024 01:36:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:7294fc90bb4e11e12b73576c796271754ea37e80f54517ad4e2899eee92cd350
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49941248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9416f53ed73862483d0a1810404cd03ad27b75f4258f13e3e43159dac921038`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:10:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c8bfd6a26c3a37b6a00ea3d238fb8eed745384d2bb98efaff22428174a68f6a1`  
		Last Modified: Wed, 10 Apr 2024 01:11:44 GMT  
		Size: 49.9 MB (49941022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87a9587bd8ac697894d9ddf850aae20937f6ae354d4f58c377b238a4c01cc35`  
		Last Modified: Wed, 10 Apr 2024 01:13:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:f16afee6d2c5b9850bcc369203d761e826a30f007a09cd0c2d7962b54149748c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51141650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75416fba14fb1a99454668de6bb4ca0d8a9354daa7d6cb63a862c9aeee814ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:25:52 GMT
ADD file:90e106baf8019819d61f3875a3695b4ee1f0f47f890bc23db62485c13c0badfd in / 
# Wed, 10 Apr 2024 01:25:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:45:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:111a73d2cd21eab548d0ffddc9bb5a4d0a8616f2cef311480858e7b83b040f90`  
		Last Modified: Wed, 10 Apr 2024 01:49:40 GMT  
		Size: 51.1 MB (51141422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f0b79d28716d75d9d1174d0a5b6e5c7c8fa4f4e2376e92023052fdffe568e2`  
		Last Modified: Wed, 10 Apr 2024 01:51:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
