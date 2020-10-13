## `debian:rc-buggy`

```console
$ docker pull debian@sha256:a5ecdde4df54accf4bf70ca7777e0ea8ad539b050edb96b56d7642d68da13d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:b878ce38bb4b70ab3b45920de342b00931c41e677e02d0e6fad38ba273397cd6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52488318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec7128bee529054d2e1e1964c42bb1ddce228924e5248256aa31892340d2267`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:02 GMT
ADD file:d09d72986a18210fc325abfbe18d3d35fef6de8ede47304410bea7528e5ab5e6 in / 
# Thu, 10 Sep 2020 00:28:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:32:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5da2bf34dd483faff62b98f29a31447619812af8afb0cdee07c188e866571393`  
		Last Modified: Thu, 10 Sep 2020 00:35:58 GMT  
		Size: 52.5 MB (52488092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251d7dbd2f5b88c7c8d0ad4a40b0cb187dd681db606e83eb00b93d67a3d28ae1`  
		Last Modified: Thu, 10 Sep 2020 00:38:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:fd16f9f794e8e296356364bc36c2115e8dfc1fc117228d85e22164609cb71b3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50413770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac11ec470495fe3768ec3c463c9a4acaa05048010c87ca7b02d25335496f013`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:56:41 GMT
ADD file:9c8616d4fabe6861a7f03ec7c1849957393374004adaf865fad27fc7e91057dc in / 
# Wed, 09 Sep 2020 23:56:44 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:00:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:dd8dd816178223393e19e5b2cd1f62df2d94bc6d5c9c393d8da9f901c96e3f93`  
		Last Modified: Thu, 10 Sep 2020 00:05:28 GMT  
		Size: 50.4 MB (50413542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be15ff42ba202309374f9e7705cd94247f0e764b799e078b44b8a1c6acb9ea7`  
		Last Modified: Thu, 10 Sep 2020 00:08:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:bed92358e098fc971cdca25ec0e7527529f5b8182f9d04b6e1ddffe1f1398f15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48255881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531f693e5359a4d5683120be92e3afc64c16adb6544a20d38e8fc6f796c46655`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:02:25 GMT
ADD file:6b1218c9574b91ad91309c12b66b8a83d37f3a3ead47d7fc3a16e3c498e6e102 in / 
# Tue, 13 Oct 2020 01:02:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:06:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:107486c9309dafb8e1d046960e1dca3c02d5aae566c72f8113cbb0f1ed15f9ab`  
		Last Modified: Tue, 13 Oct 2020 01:11:07 GMT  
		Size: 48.3 MB (48255653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3cb3db0108c1e1351f2632cd32427e20ebc1c936c9385bd2a924e7a9f7b31e`  
		Last Modified: Tue, 13 Oct 2020 01:14:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c35971a3b734fb216dd85cd2194ce64fcd70d37bb26701050b24781cdf8f9aa9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50845481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d199fe90dda4925b63371b7e98c0a66b762666d3d876d8dd1e355e6245f2b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:52:18 GMT
ADD file:0b10d18375e8cd004468a07659e73e4afcd826f2808314dcc8fbb6b773c3ed6a in / 
# Wed, 09 Sep 2020 23:52:28 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:57:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:21fc4451f3aee8da37deddc4046fa3dd8ea41b5a39481b93c43bc5dd385277d5`  
		Last Modified: Thu, 10 Sep 2020 00:00:09 GMT  
		Size: 50.8 MB (50845252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d450450b8e308c2280c3582e9be1a75428337030d6ce52ba4dfd4b7b04f091`  
		Last Modified: Thu, 10 Sep 2020 00:03:45 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:b47fd49365b62339a0533dcdba017b2598659f5f8186e08f2306c6e6576e340b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53575195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c0684e64fdc779330068e2cc414b110a812dc1a5bf3f15f66bd0d60bce1b59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:42:20 GMT
ADD file:0f16119ad5399bd128cd02055185b1f534348a2ea02757438ace9e8b088822c2 in / 
# Wed, 09 Sep 2020 23:42:21 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:45:09 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9cf7fbf089a5c33a8981bcf78f935777e9a0e1340c0526fbe21a102ede6f5a74`  
		Last Modified: Wed, 09 Sep 2020 23:48:07 GMT  
		Size: 53.6 MB (53574966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ecae0a38c5122c89130f7bdcd5fb66bf04a800c4e928de364b0a28df8087ea`  
		Last Modified: Wed, 09 Sep 2020 23:50:12 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:da2b53335062cd1cca45c428d0dadd55e82cc2edeebaf3c83ecdf623211a378c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51292419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc55c5c8d0c1a66b7bb9e4f2ec677476edb2c481ea97a6faed1237facbc1911`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:10:19 GMT
ADD file:ec8eebd9c015be5ae41233496690d158f5f7d31b3dbece81b6474018168d339d in / 
# Tue, 13 Oct 2020 01:10:20 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:13:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:acfd16a511fbf47ee6caac9e14f0361f1b2a477e4e410835a21a56951f404ee0`  
		Last Modified: Tue, 13 Oct 2020 01:17:27 GMT  
		Size: 51.3 MB (51292191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fca30f0d3418767e203d816492007718dc6db5e2039a8369c583bf9d8fff79`  
		Last Modified: Tue, 13 Oct 2020 01:22:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:3c624e5174c7da7fb5468d1cb06a682b110bd771c9e914e47878a42638fab6cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56336916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe959250f77550b2e6f691defd0aef025da11c3a6d181977012b3b31c158c3ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:51 GMT
ADD file:6525cb187fc85a4741e9d9de398149d93f43e196e99a20d48f165a25a1a8f36e in / 
# Thu, 10 Sep 2020 01:07:08 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:21:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:184155505be08ee96b6e64926098f03c472ad33bae3d34b8f683480960d7b5d6`  
		Last Modified: Thu, 10 Sep 2020 01:30:22 GMT  
		Size: 56.3 MB (56336687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fca0efd2d3c8248e41756e7d4ade3e4ee6e3783300c914c3877dad6eb16293`  
		Last Modified: Thu, 10 Sep 2020 01:42:21 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:9c0da58258aac3717dc6cc77136d8e406c5e42f7c187423a9612654fdca53cc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51120511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda291190aa9b21b01e769fef1ba5ec9e6f57f9e4024f087c4875abed2ca778e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:39 GMT
ADD file:8ae741412fc2632b17f3119be3f00db5ac9da9165ec6ba803cecb706cca2e10a in / 
# Tue, 13 Oct 2020 01:42:41 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:44:36 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2f8a9ab7d8c65b5068769e112907fa3def6a9a81b79ba5632dcc28f6bc45c59d`  
		Last Modified: Tue, 13 Oct 2020 01:46:00 GMT  
		Size: 51.1 MB (51120285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ef68497538ff95e8454cb8f22c399a878a3bbfba22a0384ead65b903dfdf9`  
		Last Modified: Tue, 13 Oct 2020 01:47:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
