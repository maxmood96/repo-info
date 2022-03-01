## `debian:rc-buggy`

```console
$ docker pull debian@sha256:de9ac60dd4a5d4ed8ce1803cad7bf5a26ecf61f6fc9b7dacf134d1b7d033db5c
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
$ docker pull debian@sha256:3b0952241dfa8150580638d7cc78460e5cc6743a08637a39b994234316171bf9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55974395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0cf58474fb9cdb67ed8445af4e5f8329cdf49f96e7b7d34d005afcf2d9a723`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:14:59 GMT
ADD file:62b7e1deca7e12cf507f0b06446a94bfbaff1760c4333fb3f8f92392b57d50b9 in / 
# Tue, 01 Mar 2022 02:15:00 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:17:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:740da9cc2bb63315fd21f4469ac9e44b2f6efbfd32f98a83c863fa9c1a145714`  
		Last Modified: Tue, 01 Mar 2022 02:21:38 GMT  
		Size: 56.0 MB (55974168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf441149e15a198263888e80394eb923d13c4c87183653a440656f39604f3e1f`  
		Last Modified: Tue, 01 Mar 2022 02:24:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:caf7f5d0056b2500a631ef111da3cc29dfb20baff2a9e02ed4cf5dce21004c8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53368686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c11c6759368047c5e43ef8d4b747b51bea9999c7556b9e35e0ce27679dfc7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:24 GMT
ADD file:ac39701f9a18e3289cda9df4afa1e6d52cc3d78e450fe0f6c8eeca44fcfbc1f8 in / 
# Tue, 01 Mar 2022 02:06:25 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:11:08 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:63235811a46a23f0266af9da0adeda5035210e9743bc381224f6094ba385018a`  
		Last Modified: Tue, 01 Mar 2022 02:23:10 GMT  
		Size: 53.4 MB (53368459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fa54141da5eebf416a083eafae7f10760cc8f2e3d09908720f9adade03e4d3`  
		Last Modified: Tue, 01 Mar 2022 02:29:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:d5c3553d8adccf86654f3ef399acaa7a414146d466274f9ad8da1bb44ae44993
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50991415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8549f6d37f8e572734f0ece5dfad38fdbb54c667a27062b393594056a8ea5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:51 GMT
ADD file:6d4b498179cf5ce76b5c392522e45f7c4c4d0d4bfecee20cf2e30c39ab2c209f in / 
# Tue, 01 Mar 2022 02:06:52 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:12:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1c659af384e72219bee43c78d09cffa65613c854ea39a8d72326f2897f1c899d`  
		Last Modified: Tue, 01 Mar 2022 02:23:24 GMT  
		Size: 51.0 MB (50991190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7182f3c8848a750405e0775de4fcb6b96917937937237b702c438e3f31148a55`  
		Last Modified: Tue, 01 Mar 2022 02:29:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0028651b01f87104dd218893075ff1c56278d199c380690792dcf3082cf8699c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54879881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1bc6c16b3ac2cdb90d7624e59b38f8337644f2b3329e09306a687af1644fe1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:59 GMT
ADD file:709038b8298e06fdef9e537e714acadf4542cec6bd98db2854a8aaa95d67784e in / 
# Tue, 01 Mar 2022 02:13:00 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:15:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6895b0cfa9016bdd8a8e291fec2a7c649679eebea9c4d2fe2c1eec8c2f512d66`  
		Last Modified: Tue, 01 Mar 2022 02:20:55 GMT  
		Size: 54.9 MB (54879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec98d2374e1080bbbf9c4e17cafc9f1438410af3c563f98a834ef33aa1bef46f`  
		Last Modified: Tue, 01 Mar 2022 02:24:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:6b9eab661b357d5d101aadafac39fb3aaf6428e161d1fe43bd6cf1d4225a9903
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57009327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83ef8662f6bed8da588c541109ffab583ef77aee7c7e132787aa03844692632`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:17 GMT
ADD file:cc05e2e409ddf6094d6143fb5d4b47dfb3390bc7281658217d6456c28a94c208 in / 
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:11:43 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fe6e66c27ed7931bded2ff21e1416e6590e3576bb223676ce7abc704e1326545`  
		Last Modified: Tue, 01 Mar 2022 02:18:48 GMT  
		Size: 57.0 MB (57009099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280a21877636329dde42224e3316db514bf26c557fc30700615b8f552dc555b2`  
		Last Modified: Tue, 01 Mar 2022 02:22:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:1aaedd9e4fb12cce1a55b327225735d8c0379514605e1c28245ac4409069ff97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54567827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab68cfc7356992cb44c13bdb329cc3a49790b4f11aeb9c106f302668c6c8eaad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:25 GMT
ADD file:203c31666290b4e65e608aeb6cf875bc54d17e55d10989248bc2e2de001c76ab in / 
# Tue, 01 Mar 2022 02:05:26 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:09:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b2b0d222db40c7856984c24ac798f37a235dcde0335158adc8c39139ae52f7cf`  
		Last Modified: Tue, 01 Mar 2022 02:15:36 GMT  
		Size: 54.6 MB (54567600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa912b634353151df5dcec007e384ecd7def05568101f1e6248d75f1eca5752`  
		Last Modified: Tue, 01 Mar 2022 02:20:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:69c45ad0cbcdbc91973800791978213cea69e67f900a04d209e7615dd0c9e9dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60392892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98517374b32984b0b89aff1a7be976edfdbc73660b3d44ed60a0ec18d6a171af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:35 GMT
ADD file:b9f003037b742d278d03bf492fdacca507aed7e40b6e3727c8e5053d83d7d356 in / 
# Tue, 01 Mar 2022 02:07:43 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:11:15 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:071265fa048a30ea363f6d7ac648ffe04d00265431517a6f41931d6009cba801`  
		Last Modified: Tue, 01 Mar 2022 02:17:38 GMT  
		Size: 60.4 MB (60392664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24a838d71f3ebcf8f78f710d1b0fe983148311aa0fe6915aae3b0f3545f4bcf`  
		Last Modified: Tue, 01 Mar 2022 02:20:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:c8c06df24cf235b45808c8ea6d0a6ab964ed9e56542cc83db3080223afdd4ab7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54226794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5fab58d2f5959d31a8a1d7eb79295f4b7e20da7f501c6e4bce94e854dfeb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:07 GMT
ADD file:2f65c3757aaa4675484ab3662d157fea03e752f3e5c0b584a7d05649e2599f2e in / 
# Tue, 01 Mar 2022 02:03:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:04:57 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b3073d0c9abbb315a4b9ae0014cf38bf506aea211bf49fa8a5cc18e3c3f8e282`  
		Last Modified: Tue, 01 Mar 2022 02:08:44 GMT  
		Size: 54.2 MB (54226570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74775e073af8fa793a34b4b6a588a308706dd1756391973c55ed0b163850a217`  
		Last Modified: Tue, 01 Mar 2022 02:10:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
