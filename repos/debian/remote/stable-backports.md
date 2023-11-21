## `debian:stable-backports`

```console
$ docker pull debian@sha256:03240e4c7aa67fa21cfb42f23f3b30861cfac3ed260c9c721e6d0af7a4a8e114
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
$ docker pull debian@sha256:91cf23d5b339363f9305eba4788b55dbd34a65f46e5783310841569463d03369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63a4c97b54aa0db2fa2cd3784f748d8c8caa980d161027ee424d562d2abcaae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:30 GMT
ADD file:789d25d98d9623e204d48a1f8267ce4340ff5fb9d822539b73aa46f006d70387 in / 
# Tue, 21 Nov 2023 05:23:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:23:35 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d896f38a2d4bfd38cd073758db4158c6cb493b70cb46bdba665973165aac3025`  
		Last Modified: Tue, 21 Nov 2023 05:29:13 GMT  
		Size: 49.6 MB (49582212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830b5e33380fac5b23ddd31df85e28acd3084cfd69b84ed0f57ba36ba2c26419`  
		Last Modified: Tue, 21 Nov 2023 05:29:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3f96dc95967f40311dfd2066c4049b7b24bf507a7768bade31b1baabded04c0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47355973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18e52588bdf88d507c8e82431ab7f6611210056168917dc32f301860f7a14c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:01:48 GMT
ADD file:05d4f483ed515dc47d5bd1f7e5e90bc3d02821818848c5b00f52d37f6f7bff4e in / 
# Tue, 21 Nov 2023 05:01:49 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:01:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e02f47df7e9ddc4b1f964075a0833af0f7a97a67f6ce871d216de797408d47d`  
		Last Modified: Tue, 21 Nov 2023 05:06:06 GMT  
		Size: 47.4 MB (47355754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4799997a13f7946213c2709836ccc392f10f18e31f8a210001580172f37e5358`  
		Last Modified: Tue, 21 Nov 2023 05:06:14 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:753de1e18aafaf319a010ee1aeb33c919fb550aaaea4f64f1a8b5e95450021a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18e0373d77b1984bc765ce8c6f80a295e6fd23a4043128e8c4ab0a420b35b00`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:21 GMT
ADD file:9449e70119877a15c4e32fd928c3c66d5ef3bceb73ea3ea9f42a9d37c35114b9 in / 
# Tue, 21 Nov 2023 03:59:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:59:25 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0681e3a8af101f8eacf74d0544d2d3870674cfb10dea2824fb7a397fcd472bc4`  
		Last Modified: Tue, 21 Nov 2023 04:05:24 GMT  
		Size: 45.2 MB (45180053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8d0fca79629165459821f8238ec1fe4ae3a1172c424e876e413a7e5133ad3c`  
		Last Modified: Tue, 21 Nov 2023 04:05:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5378522099b93d046f24ed02a149b8fc75802aacf2ea6416549e1ecfd00673eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49612846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8aec5523d8b744905c19f1273490d329163e3e451690e65b5f50649da5c2417`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:22 GMT
ADD file:0b58368d3350a8246327821d9a6551fb2b29ca862f33def8ccf8cbd64af9318e in / 
# Tue, 21 Nov 2023 06:28:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:28:25 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2fae27f6b18220447738106381fb8bad7536ad7de2e1fdb7bdb63d5d5dcc3a9d`  
		Last Modified: Tue, 21 Nov 2023 06:33:30 GMT  
		Size: 49.6 MB (49612622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc872e389071d6695447292df146d136107d888fc45476a2486ca0e95c579b4`  
		Last Modified: Tue, 21 Nov 2023 06:33:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:8ee3628469fa4b2ff564cc1a55a673eb31f871889926020123a94f67973f1dcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50601063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca66dbb364fd44c365b4a293f48c49f6102039737bf12da2f46ab1a6b400ab2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:41:51 GMT
ADD file:02448fec868d4ead9c9ba4522890527fae0a8383d230ad96d1332711598c24fd in / 
# Tue, 21 Nov 2023 04:41:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:41:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1a62b4e81c4807ef7dce246f03cf8d5229c384cb52b6bdfb7f1df20e7812678a`  
		Last Modified: Tue, 21 Nov 2023 04:48:26 GMT  
		Size: 50.6 MB (50600838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6cd865a296d01caa915fcf79779c4df0c5956e378ca3ffcff89ca1e7818beb`  
		Last Modified: Tue, 21 Nov 2023 04:48:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b07cd493cde05727e40aae8dcdf2b9afac95cf137b0ff9216bb7f05ccf4feaff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a98d0c9b4982500fb10abd555efeb9019a3d6bf8bda0672e2adec3fe8cee14a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:13:53 GMT
ADD file:484363709951b76cab1fbf3e7caf4f006bf1917127ca9071365e8ba20c80ac88 in / 
# Tue, 21 Nov 2023 04:13:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:14:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71826ad9cef5309b30c1a728078ce3b7e80a5780a5ccd856baa4c9b62d4dc295`  
		Last Modified: Tue, 21 Nov 2023 04:25:06 GMT  
		Size: 49.6 MB (49569201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef25057da3fa431d898ed964e4ab60daa84bb674e3b118c298bad4c5726fa6`  
		Last Modified: Tue, 21 Nov 2023 04:25:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0089455ec515c578003377682d3770c27972f686148f888e23227ecef935b9b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53576088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91050186425ec2441cd5f9db5b9ed0869d6af9c350d41b7527f55b4974d99ce2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:55 GMT
ADD file:0c91d476365cfc1076554245768ff131f2899b3b3b92d74ab7dcc15a437f21b0 in / 
# Tue, 21 Nov 2023 04:25:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:26:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c60bb382b41113221545d52eeea57e75cc0d76f056c6e31a991f40e504b6c040`  
		Last Modified: Tue, 21 Nov 2023 04:31:21 GMT  
		Size: 53.6 MB (53575863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9b3285334dda10b628f8184247c2abf4f5e1e47f3a6ff52ba873f3eadaa06e`  
		Last Modified: Tue, 21 Nov 2023 04:31:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:fc3f09a181d64aa037d26c0cd1c5a3f0cdbec35ac47e9b5429beed61d1d8a6fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47943193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a12c985946a3fccb869807b8ea77fb23113b46aceb7bcee136ec02b07a9922c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:38 GMT
ADD file:2fd0e93b36db470b65ddf3b3154e08fdc83f8c65f16f5dca7aad699d3d818561 in / 
# Tue, 21 Nov 2023 05:06:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:06:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:21aed744c180fed5f9182e7b5c77c7a665599380381860720095e8c30e16661b`  
		Last Modified: Tue, 21 Nov 2023 05:11:41 GMT  
		Size: 47.9 MB (47942970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252b1f491c41ed85897037a5eca99c19d6814f7f48a2da7c1cae7a35b9cd9ef5`  
		Last Modified: Tue, 21 Nov 2023 05:11:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
