## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:060eb719db49c0d08c3823e95586f03739b9ce53b51af5f2d062e3a1dd0b1c13
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:e9e9a26099b9004fb06f6b01d26db24d06e530b810cbcb62af0b8879fb43a6e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54868482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab17d80723e93f59a4f54e8176c5841404dc3d2d7cf8d2f7126453ffd98d405`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:19:44 GMT
ADD file:09ffbc0a4ab7c70a3071740e19113a2f2d61593241bfb8455aeeea7877b8784c in / 
# Sat, 10 Apr 2021 01:19:45 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:19:49 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf7e31f852204930ef60bd4c12f9606812c0b9ba6235e2e46e1a5900f2db9d30`  
		Last Modified: Sat, 10 Apr 2021 01:23:56 GMT  
		Size: 54.9 MB (54868257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9203333e7bfce6418f835e0928eadf5e1bc8b829047c79072f6515b142b3162`  
		Last Modified: Sat, 10 Apr 2021 01:24:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c6776530ac463ca7989418d025f92844da1caf0ea3e1a915ef752117a40389e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52401675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0ee79835d3e1dff9779ff576f672e78dc7eb8d76a7a540737882e9e4213e51`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:50:12 GMT
ADD file:37fd08ef57f840011e25ed9f68d8b5197a5378b1f7bebee7fa587d5e7d561844 in / 
# Sat, 10 Apr 2021 00:50:15 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:50:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3c6e089fcab6bbe7eaacf21e4d0c43c7da8b8a21cad425a714fbb8d6798ccadc`  
		Last Modified: Sat, 10 Apr 2021 00:58:12 GMT  
		Size: 52.4 MB (52401447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a6027c7cf1c8ed8cc5061ffc94949539b3bd5d9c7c764736bf8d06a7ebde4f`  
		Last Modified: Sat, 10 Apr 2021 00:58:25 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:578a0982f0fc836c8987d1adce3a5d021b29ba353d2e994fe5d90fab47ccc596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50070575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2574f651e0887758d245ccece019c0b51819a29a27788098a39705c11521e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:58:24 GMT
ADD file:5e17f4d5cdf1ff091554ccfa33e22ab2be0c278b0cec1c11b45333deda2cfc79 in / 
# Sat, 10 Apr 2021 00:58:24 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:58:37 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df95183d3a18fe92c278757657c6fef8fcc11f2a9a578df2f2b00dbccf0a8ea6`  
		Last Modified: Sat, 10 Apr 2021 01:06:36 GMT  
		Size: 50.1 MB (50070347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ec3a3134e6af742b736c17ba1137c4b8cd180314ed840a37a273c8a769ce1`  
		Last Modified: Sat, 10 Apr 2021 01:06:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:de1229ba5fa3bd1c907f8e8b5f519b54d082bf77e5ebc296c0ed3806cfa7926c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d825fd8b2336438f6c75306ad791236056a7d2c9b7e39069375f0ba5cc74cd8c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:14 GMT
ADD file:e1b7ed0c35932136d6c29369c3eb387896a482b3b227f18462715ed1690af4d4 in / 
# Sat, 10 Apr 2021 00:40:17 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:40:28 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a5ad85c1142d6ba07dd2031cb0c6c7513422a29a4e0446b232121280077ee9eb`  
		Last Modified: Sat, 10 Apr 2021 00:46:54 GMT  
		Size: 53.6 MB (53555409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19931e11df4f192815a3ed9ceae93b13bb01023265843d00f1d86b2e90966bf8`  
		Last Modified: Sat, 10 Apr 2021 00:47:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:2008962d45eae751922f439f9a1ff1735fdce7ce076606505a67df07937704c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55881608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e6b2bbd7bb7e24fb2ca7fd254910392710555323d01c078574aa0c43584d4f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:38:57 GMT
ADD file:72806e483423c962f867acf22783e8b91aa9d8486d1d35505eaa5442df41be57 in / 
# Sat, 10 Apr 2021 00:38:58 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:39:04 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c73c775bc05dae13d9e00c5c3e6660d213997be492a06abcfe494e5fbfe97f21`  
		Last Modified: Sat, 10 Apr 2021 00:44:36 GMT  
		Size: 55.9 MB (55881380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c837ee223a6a56e31784abbf88069ab4a0bc2571e37be9f8c57b0e4a2674e10`  
		Last Modified: Sat, 10 Apr 2021 00:44:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b8f9a9fae7b519d07671952c4f1740cb01699aaf9b194f22e3816d22aa4b0f73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53127623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45d200e228b115e2b246e1b368eeb81fa977c239e099a92702da5aae44285ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:08:30 GMT
ADD file:05ecd203b7e6783fda8a687a6d061102831b24ebff7441f9b8bd407ea76580fb in / 
# Sat, 10 Apr 2021 01:08:31 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:08:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f35fc328cfb1004badf99abc0ffb0868b98173f9361dc1a1a0fb16c971579044`  
		Last Modified: Sat, 10 Apr 2021 01:13:59 GMT  
		Size: 53.1 MB (53127395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64640270f4c9a5137ba3e25ee364fd06415900caa4993dd58f6f43517cb26919`  
		Last Modified: Sat, 10 Apr 2021 01:14:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ec92e77d35aca5323735b8473274ef34f055cf741f1a81ae28c0db56e2c1e685
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58783473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc39b7a423718374fef3ce8f2cac32c60c85d0606093c0bd341baa023c1b7e9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:24:22 GMT
ADD file:c677239aef001babcb1663e8f2e9aadd81b7da6c581bb55368efc93625140098 in / 
# Sat, 10 Apr 2021 01:24:32 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:24:57 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ddef5f25272167da6de06606c43b7762709f7f2d95d2624ba3d2adafbd2d13d5`  
		Last Modified: Sat, 10 Apr 2021 01:32:37 GMT  
		Size: 58.8 MB (58783245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d445832530c5eaadd4f41e500178754dc7e4c025abbc220974e90e833942c6`  
		Last Modified: Sat, 10 Apr 2021 01:32:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:afc13bb135da5927916a5d65c7d984043ad4348b3f3dbe46c5d67bfeff1a4e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53148497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de76f33bc2f26110a33376f5606afdb4df0b1c2585b05b0eba415bd4da18b0a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:38 GMT
ADD file:5e12a744308594a409852feb52fdce1bafd5db69b42d23f30da5fd5da36c7900 in / 
# Sat, 10 Apr 2021 00:41:42 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:22dffdd7e7137fea3c673394c15d7ec19300c9ca95cda64cb366ed192a6a2632`  
		Last Modified: Sat, 10 Apr 2021 00:45:03 GMT  
		Size: 53.1 MB (53148269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830bea06ac419cf2282feb3e30978baea434e0fd4a01711ba657563af981e0ac`  
		Last Modified: Sat, 10 Apr 2021 00:45:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
