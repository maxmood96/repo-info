## `debian:rc-buggy`

```console
$ docker pull debian@sha256:558c4039457cc61c0d03349eb8390a88ab9ab479b19c542dc53f749f90bea45b
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:084afe14f7de8377c103633a7cef1156291042df88cc2d4c755fab5ae1c0c361
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50311567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49beddb01f747ab1d6be388f47e0fdbdd8148266157003ee77b7cbed74b37da8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:42 GMT
ADD file:ace32e845b2ef519c79a725518e909bcbe50ecb496c1dfc8e96fba83ffaf685b in / 
# Tue, 15 Nov 2022 04:05:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:06:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b6bf34ac41ed5383f401a5e77ae46b55249a145be0fe8eb1bf8f0e4f7febfb2a`  
		Last Modified: Tue, 15 Nov 2022 04:10:16 GMT  
		Size: 50.3 MB (50311341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461c4ddb5754b70987d43cc532b6c43acfd35ee24c15997c1bdbf7918db7b1a8`  
		Last Modified: Tue, 15 Nov 2022 04:12:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:637f36842aba789c9876cb18f01c40957e8546c1ff41407b6a8fd187f3bcbee7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49284385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc91572ff9cc6f0cc1761493758a335bf9401121a018ee483f5b33c16874a15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:31 GMT
ADD file:08f8312faaa666d9d1d3cdf1e0ac577979317e8784c264b29b4d3399045d2adb in / 
# Tue, 15 Nov 2022 01:49:32 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:51:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:351340891f63641ac5516af46a2dfb6b370ea5971d604352dfe16a498646eb52`  
		Last Modified: Tue, 15 Nov 2022 01:54:51 GMT  
		Size: 49.3 MB (49284160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155315c6b175972bd2db327c3d66c4fe9ba7fda58823af50a289700fae553901`  
		Last Modified: Tue, 15 Nov 2022 01:57:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:ddc5f4da781c6cc7f1531606c32e20b632ca437e7496311dde1ab6495f4443c0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee1df29ae20ac0fc301cc28cb7ba08a72feb7d0209e429583bfec09576c4fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 03:44:42 GMT
ADD file:c9d57eeb50bde8da5c06a8e258d811f84122cec325dcd8c9c1f0af577a00b5ae in / 
# Tue, 15 Nov 2022 03:44:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:46:31 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7d8a148f561149045bbc5d86c167ced3751471156eb66153a1016778d252dd2b`  
		Last Modified: Tue, 15 Nov 2022 03:52:03 GMT  
		Size: 47.1 MB (47101515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6715cfe4f5bc6e023897af90bb5793fba5b3f794602bc867159bc73ba09c55c5`  
		Last Modified: Tue, 15 Nov 2022 03:54:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5fa279065942dbc26f743b317b883093b6cb8ce35ed7aa8fa86bb831ac82a7fc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50371403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723da4aac1cf495afbce06fcb994ec2fc2def11f0416feead2adc4b1d45d0fcd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:54 GMT
ADD file:ba227e9990636bcf4ac74991aee2f89f076de2adf7a651c75b55b2dc145b5340 in / 
# Tue, 15 Nov 2022 01:41:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a4831e9d6ed52920992a4dda63cbeb8f430d77a27377294be499a02b93fb1e3b`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 50.4 MB (50371180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a07492a85e28b785e45aab36694235c684a32de79d0ecc8e7121398f910f957`  
		Last Modified: Tue, 15 Nov 2022 01:47:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:2f0a6496a6be0a955a75db01bcaaa70dd8f023c60a0f12188e3e0c9dd2d8ad52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51364319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9d1995822d55fc15c1c867587e859770639937fad5063f29004844ee865e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:30 GMT
ADD file:6c7cf2ddf77e13ddd1b27b3e2895b29bf27b8fd6d38de6f5fa7330138f69523b in / 
# Tue, 15 Nov 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:44:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3d85d48acbb26d22f92c31ab4d483ab5c9fc0a7db5f67806b2c05a4460060ee4`  
		Last Modified: Tue, 15 Nov 2022 01:48:49 GMT  
		Size: 51.4 MB (51364090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f13d4021df038e16957b7ae89d36a3524618cd2bea3c0c985dcded72048762`  
		Last Modified: Tue, 15 Nov 2022 01:51:06 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:4ace5749313900dcced0cfc83a1fcc9b5b0e9181abe39b1b1cf66a5628f972e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50328659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3a41fc6e546bc8475eae73cb61b2cc191bf8aa2aa09ec1818711b3e0c404b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:14:16 GMT
ADD file:c60a8c207626b9bb85c6ab0f734c92f0094d59427717e2d7624cb29ccda64e03 in / 
# Tue, 15 Nov 2022 04:14:21 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:18:12 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:facbd376e86382e65b5fd1d879de9db0a46c5412257cfa0e54979c08f55d5d76`  
		Last Modified: Tue, 15 Nov 2022 04:21:57 GMT  
		Size: 50.3 MB (50328430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4162277c59abb9afef6cb7de3e70fa13117bab9b38a09e1037147a17b8f79235`  
		Last Modified: Tue, 15 Nov 2022 04:26:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:a4bdaa071f51ea9408f08af93d3a660926aff63aeeebf2b3eff1f1b2ff8a108d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54704944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314cce142adfb2c259db653ad2754fa311523124c048c50e87032a4140a35d5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:07 GMT
ADD file:6e9efd6bb77c835520332c88cb412f38f0d8573ec3347b090b77965e17131780 in / 
# Tue, 25 Oct 2022 03:14:10 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:16:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a3962f6ac5b86fa159789ea1e9241ecbb956b3223e8312f7d92d7fbb8bf5485`  
		Last Modified: Tue, 25 Oct 2022 03:20:03 GMT  
		Size: 54.7 MB (54704717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea915dae8e4e8fc1d71dda087fcf35607312c2e52a161bf9a3b775326ea7831`  
		Last Modified: Tue, 25 Oct 2022 03:23:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:7267909683fc78ba2b04cd0203e985d1185adf90742f7531a0025e35e71dbc19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48717119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37a12a6c3ae821f3f1f5ab93e6512e4f3930f942f016c19559b98c0ec611490`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:43:11 GMT
ADD file:47253af7a4fe925d592c8b6d41b8dff6122bbdd083ebe6ff091bd90271f78b19 in / 
# Tue, 15 Nov 2022 01:43:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:45:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ba49eb7f21a2367672851b25b6c120e1a153fdf9884b643d9b288f026a56ddcb`  
		Last Modified: Tue, 15 Nov 2022 01:47:50 GMT  
		Size: 48.7 MB (48716895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edee461ddd146da6989a86fa8cea3f6c0c8ea15dc9e83d1144a89eb2e203fd18`  
		Last Modified: Tue, 15 Nov 2022 01:49:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
