## `debian:testing-backports`

```console
$ docker pull debian@sha256:f507d9d22e84e0efce537db916e0d2394c4e754e909b71e507098cc445bc2263
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:50a2dec5582f9040547286a3af03ff39aa246b958048e1e6936339ebc4946fd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49539025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72d7473d6330c9313590ba1ca7eabd00a8a2bf8c46f0a90383ebc4e1d30bdd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:51 GMT
ADD file:9bf7047d4bc565e7e2cb1baf7275fe6b02fc9e4627e500bb4d7c8cd739a26aae in / 
# Tue, 21 Nov 2023 05:23:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:23:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:786c9ee75a8d6bb4c357dfb6a4cff0b70faa3dd8a36a5024897ebb5c8c6cbba9`  
		Last Modified: Tue, 21 Nov 2023 05:29:45 GMT  
		Size: 49.5 MB (49538803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317d8c94d57ac466aaa97622a78e27d532d7e8a4d7e49fb531a5f207bad77d8f`  
		Last Modified: Tue, 21 Nov 2023 05:29:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c659f1c9ab5da45504c312c2b6c7b7dedcf70a44b659fbeb2b86633ead851d85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47222487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70f18ce16699da79d9146db47404576d1bb2f6aa451ab315187c9a554caa598`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:02:06 GMT
ADD file:7d89335b47bf003eed49a50141992d44540a6839925952f6df869c5ed2e73fae in / 
# Tue, 21 Nov 2023 05:02:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:02:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd280b62f0f2a1f2404832810c0658e36030b0181eefb3280190bb79bc2f1fe6`  
		Last Modified: Tue, 21 Nov 2023 05:06:41 GMT  
		Size: 47.2 MB (47222265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6565d528e90dee0a5c7441c86a4fce3d533f64c2a6adfb605914a18bf9a79df0`  
		Last Modified: Tue, 21 Nov 2023 05:06:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0428a7bf6235dad9ecc8a49d9337832d222f9956110ef93af3af173d29283dc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45026002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9a9ae3f39e926cca6be0773469e60abeafb0853b876e5cdeac607ea6fe8ec1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:40 GMT
ADD file:4404bb0a7caa859eb6792b4c7f2bcb915896f903b2bc0cff5568f5e43400e4b2 in / 
# Tue, 21 Nov 2023 03:59:40 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:59:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:575959dd9a02fb488f355597694e6b863c4df87a17497d74140ba7879044c141`  
		Last Modified: Tue, 21 Nov 2023 04:05:57 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3d5176ed8ce860887870dc013cb8699f6b6c49da8c3c2f6bcd3e9988108385`  
		Last Modified: Tue, 21 Nov 2023 04:06:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f79e511286b236cd7611dcb32db5751c814a428265486d928827b05498621d3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49571502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6748aeea98ae9b345ef694170af3fef5a47a5cac9330f77789ccbf21c29f469c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:36 GMT
ADD file:19f717739f7e55ba067aa6bb34df0d612deb5f8c2614311d867f5f6a987beb96 in / 
# Tue, 21 Nov 2023 06:28:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:28:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b331fba2b83cc1c8a6d0cbd20ea0869610ed9049598db306ed9a572e23fbf94d`  
		Last Modified: Tue, 21 Nov 2023 06:34:03 GMT  
		Size: 49.6 MB (49571279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247b269edb6621dfacc09c03480af2576e3ab2a6ba15768677a57e582a21d253`  
		Last Modified: Tue, 21 Nov 2023 06:34:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:02e8d37849c7d136888419d1717e84099f8dfaa2b77c2ee872dec60d61565b59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50516305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33828b388dbc2de1c230620a7ae472b29683b07145ee6345609ae9407d3d97e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:42:12 GMT
ADD file:23e10a72ed2309bd745effa25d58a1a965c4913c28f9b97173ceb39c107a5d52 in / 
# Tue, 21 Nov 2023 04:42:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3b47b63c7f6109cb32403691af9ab3d1f9f9a11b7ab9bed4eb3a6729539d3dbe`  
		Last Modified: Tue, 21 Nov 2023 04:49:09 GMT  
		Size: 50.5 MB (50516082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9ca7d4a96fbb6cc8b96d586780bbac6ee95268e224d77b6bdcfeb0054007f`  
		Last Modified: Tue, 21 Nov 2023 04:49:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:eb035f07a3923b353d9c7f00003eb70b87745d69918c3212cb9e1230d34f3add
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49327750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0736be6e5f74ede41181bbf030f5b7b630ba36d64ff189c3eae50577fb5fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:15:05 GMT
ADD file:1ffa8c6fee5f3cf0abcaf587ceb4926c3c8f2c831d0e716b9e5f364201b579e9 in / 
# Tue, 21 Nov 2023 04:15:09 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:15:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bc698a70e0be05decb91124acd6250a7c421eb2d3c99eb42fb1eb36846b2982b`  
		Last Modified: Tue, 21 Nov 2023 04:26:18 GMT  
		Size: 49.3 MB (49327524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e252d04155d00b0009c31239523cf742e519815636d83b96f0634466837955`  
		Last Modified: Tue, 21 Nov 2023 04:26:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1abf147f27f9767933b3f5c8b62ed27a879fa4b6763beabe3e98bf11ca2456f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53438106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5b24a9d64f1aa029ba342284b750aedb32104c3e35e828eec08acdab87eafa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:21 GMT
ADD file:71d427bbf9540f83121632225a69e48179f2f39399ea9fd6fecee1c14a31ccfd in / 
# Tue, 21 Nov 2023 04:26:24 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:26:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:98137b81bb887133d8b0852640651013383090ed775e3e79027ef2fcdd4c97ec`  
		Last Modified: Tue, 21 Nov 2023 04:32:02 GMT  
		Size: 53.4 MB (53437880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f50158eb08971402dac7b58762e158b565bd22e05a8ede3f90a9260ebc61e1`  
		Last Modified: Tue, 21 Nov 2023 04:32:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:787053254556a978a64052b51bb39f68506e947b312ec900dab6c7c963366ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48970470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cac3166a327896bf2994eeaf60680ccdc0fab3917a17fb327501816935fa25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:18 GMT
ADD file:6bcc5494bc5ece86858cc0a9db1f3dbaed7e64670b3a78b5868b8795646fb7c4 in / 
# Tue, 21 Nov 2023 05:07:26 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:07:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f502a1e486510d668a00f33968ab7fd0960f1db8c92e8904a91b1b728da08811`  
		Last Modified: Tue, 21 Nov 2023 05:12:03 GMT  
		Size: 49.0 MB (48970248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d06b2a63737dadabcb446c9ec3fa0e1f1382b75048a64bd0c70313beaddfd4`  
		Last Modified: Tue, 21 Nov 2023 05:12:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
