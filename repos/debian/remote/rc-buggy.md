## `debian:rc-buggy`

```console
$ docker pull debian@sha256:f6a16e97023cfdb482019de0c91f6d09230e30e18e2eda02aabc8bc0f20a240d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:bb7d1223b7c2f3d4478af06621311a9a24a0f1922240ebf8896e8b95e72d4ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48712238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d86194bc4f9c559bfc41433983df67ce9ea4efd064527a711ba64175c6c09e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:58:10 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ecf50a7504ec0ab62492a074c3626d311fb5428298204e58561b37dd16f024`  
		Last Modified: Tue, 19 May 2026 22:58:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:ee2846dc81b09f0f2fe31a37a8e62b57773bc3e67daf22424ddf184ead5a22b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e21379e83c3b878e8a3819b931bae11cb317861f8eff2ccd1a90c2cf8281b4`

```dockerfile
```

-	Layers:
	-	`sha256:055b49032c4eb9593f1c239ca41ba51e035ddd5cc0a196ec924ba8f54043f892`  
		Last Modified: Tue, 19 May 2026 22:58:17 GMT  
		Size: 3.1 MB (3145072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb70d4ebb3c5e2d5976f55ea0d1dd934ea1d71d23a739045413ac9c404ef6e4`  
		Last Modified: Tue, 19 May 2026 22:58:17 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b44a1050a4a0e894b97d49080d4e4d70dd411976d955892f1e62879d8761048e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45619181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed38e262fa4b287f17a6668b75dd6b42a561e8aab9fe9d8f3e7d16492fa05e01`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:57:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:1c98d9ac4796e25c1d81c99407f882de7bda76effb4d3c6a5d937bf755cc2313`  
		Last Modified: Tue, 19 May 2026 22:36:23 GMT  
		Size: 45.6 MB (45618956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab8a5c1da0df973ce9fa55c45019bebd2dcbff051d56c2af8f81ecfceaaf50f`  
		Last Modified: Tue, 19 May 2026 22:57:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d100d2c77d21f069294d018213bf7fce8aa328a39bb554480b34af8798dc053c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d115c1fb66caeb024cdb6dd5e7a8357f76e722ef8a7a4421ae5d1e2b9c193c98`

```dockerfile
```

-	Layers:
	-	`sha256:3dbfcd7289547a695fe1f5a163d227332de668a2c3aa8d37f7897466b0e4a36a`  
		Last Modified: Tue, 19 May 2026 22:57:45 GMT  
		Size: 3.1 MB (3146442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f043e7f0228e9e5692ec46545cd2bd196fa971aa3134529cda9912a54d93a8c3`  
		Last Modified: Tue, 19 May 2026 22:57:45 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:273d54b9b0bc71d413ff128fa77dfc745194d4005df278570334dd920baa0725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48737835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2aa4cdd1edbe8dd5c405c2a6633c8ed9b8931c0bd8145586a437a3da334524c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:55:57 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a13a86f2e86f31def4cd49c8812187dd680de396f8b891502183cda8259d33`  
		Last Modified: Tue, 19 May 2026 22:56:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:7c06d1205a5fc3b218fe354f8da8779dcab5bce8efc8fa02d32fe075c7b49cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1581ba7d3b11c02e3fa4716581dd8fc12279febb3c5372f0ec8cb9e4d63bff`

```dockerfile
```

-	Layers:
	-	`sha256:0bae4ccf03af49e5484329d5dc6a1e7200acc42463b4a2ac5c300dfb80654e3d`  
		Last Modified: Tue, 19 May 2026 22:56:04 GMT  
		Size: 3.1 MB (3149754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1db1db9160603992f1ca06a0f68d90e74d5c46436fc6c5fdd300ea9307b9dbc`  
		Last Modified: Tue, 19 May 2026 22:56:04 GMT  
		Size: 6.1 KB (6134 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:09a6e94ebbd6fd1d4a951476ed4ea055a76fae7a2f78ee5b3d74c54665167b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50016233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c67f9fee1136f83bb4e74c4b8fa4a4e8f73f52d84f39c18f36020183a2ee35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:57:54 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd80e0ea874f06e25f3970a64b4e02b5685575d4048cc1ceece581cdf49a944`  
		Last Modified: Tue, 19 May 2026 22:58:01 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:c7cf685213dcd0c87d9b77e1a3706143e38509726b4e6513fe786ed508f6a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd8852f7bb784b8cac03a2eddf07066982f66abb956939ed8bf6524f0162313`

```dockerfile
```

-	Layers:
	-	`sha256:a009b7f621b318f98b3d971fa49a95d7da4ea4d5550c395fe634d9665fa8f747`  
		Last Modified: Tue, 19 May 2026 22:58:01 GMT  
		Size: 3.1 MB (3142266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdcdc25be489638da6ecba5038bc052e423aa710424ea15fa837909a93a65df5`  
		Last Modified: Tue, 19 May 2026 22:58:01 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:2596d120f3fc0763958af83e3889d21bf1c457d46fcc6fa2836bc7bdbb2cce10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54046348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596660fae76660d9cfb27ff2fb25af3a5a40d513a9910cf00e52569fa5d6ac8a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:57:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0bda88a8fa865607f7a3bfe01b25fa99681c2572077bbfaf6b7e16e1f51b5b50`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 54.0 MB (54046122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fa55d9bfda937f854aadecc43e80392689ac4cf3d469274dd108a6cb24b88c`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:c3ca163c29a2fc5da980bd5a496addaa1cae9c17108e1b1aa9c04c56baad489f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2694dd20715b7cdfb71311d18c859b64d442cd2aca098a6e24b0d1cf8ffcf51f`

```dockerfile
```

-	Layers:
	-	`sha256:bae3757dabbf83fcd64be41b1fc276ef844ba714d6af9788ced573f202e8ac7a`  
		Last Modified: Tue, 19 May 2026 22:57:18 GMT  
		Size: 3.1 MB (3148585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191f6627d54545e891e46061eb43dbeb9100890bf29874562f941c903d780668`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:671df20e38881595d9aae2b895a2fa73c1f7784f96bf93783e7d54343bf7201e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46808623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ba03718a25cdfb79d47b8e8fa80dbdfd24ffb9b8e0a5129cd31b02741f1419`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 01:53:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d609dbe8a64103ca9a52594c54358bca867134ca11c5bdbab5024849e5765438`  
		Last Modified: Tue, 19 May 2026 23:39:28 GMT  
		Size: 46.8 MB (46808398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d2d041bd6bda77686d57014db197a623dd9fc68cf6cb4ec5300adec86f95c1`  
		Last Modified: Wed, 20 May 2026 01:54:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:8f7ced750b15e09f4b732777a2b329a8e33c4454b73e8d3adedb25ed0447a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6256e28a2d1c2a0d7470807efeee79982ae332243d1af8cbaae34f4a87e3534`

```dockerfile
```

-	Layers:
	-	`sha256:3f51651757f3de963e5a012939139fc55d65f4e39732b8e9d21cd4c7e0cfa8b6`  
		Last Modified: Wed, 20 May 2026 01:54:13 GMT  
		Size: 3.1 MB (3136588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637296b259d2263737f1073aef8e8ee5da06ae84adedef73f5b6ae60d3286efb`  
		Last Modified: Wed, 20 May 2026 01:54:13 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:e3c3171cce13c90bfd22dfaff3de909c21482db31a5f51bc58490f45e26bea98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48454479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cb1a3164c8848639d78cdaf133198c1b7837a4ef78447deaab5ac915e3f32c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:57:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b2de0004fb71a1e4abdd27d0619b3567a865a43b4039f4f3ca7e11b6e7bf8ca5`  
		Last Modified: Tue, 19 May 2026 22:36:09 GMT  
		Size: 48.5 MB (48454253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2fcdb5b72757af359cd05bc1cb2b6f5a594117a3268b7b491adb21dcd5f816`  
		Last Modified: Tue, 19 May 2026 22:57:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:0c0da9973b1c91aca54a838deeea560c8e87775a9997ee37426c9b9128826ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b187ce00182a9a09f727cce39aa7bdc9952d2f727b2a02d930bd43571767a50`

```dockerfile
```

-	Layers:
	-	`sha256:cb905c97b8e42c625be9219561ca8f1e310c9e31ede291a1214583436159016a`  
		Last Modified: Tue, 19 May 2026 22:57:14 GMT  
		Size: 3.1 MB (3146523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9002a04457e4763ad7c78658bcba30574108e8ff81a97396e7d8786403bb1a40`  
		Last Modified: Tue, 19 May 2026 22:57:13 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
