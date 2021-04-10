## `debian:stretch-backports`

```console
$ docker pull debian@sha256:db715b886b3e6410d64252590e1e4ab77c7a56b3e37f245481b0d601670f57c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:2916e55da1a76c33d39f918662c8c2d6f46b5b4f3319ea708405219abe52fd43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a681d26e117e7fe379b1a589d7ec6b39cd3187416b664d2b6820d1e83b50ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:41 GMT
ADD file:e3d37689e896a83d39040f2c95091ff88f3899b5b410dbf76908dd6c938b8cb5 in / 
# Sat, 10 Apr 2021 01:21:41 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:21:46 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76b8ef87096fa726adbe8f073ef69bb5664bac19474c5cce4dd69e08a234903b`  
		Last Modified: Sat, 10 Apr 2021 01:27:52 GMT  
		Size: 45.4 MB (45380037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cf9419cf23487fa3fa56792228e6c15b0d3fb0b4374b8f04f816a05d974ca7`  
		Last Modified: Sat, 10 Apr 2021 01:28:09 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f8f552637b2867ab1567d8a04a218d41683541a5e52d092149a808bc887b37cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae135d1701239288664b977a43ac8f5393a84e1e2261cd224fe77a44225a2022`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:54:22 GMT
ADD file:2fde330dbb713eea654f455b487331e4137626ec1c35ae3aa85c3f491f38e06b in / 
# Sat, 10 Apr 2021 00:54:25 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:54:37 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:af7c3baa863c80017202aecc5f5cd17980d74282a48ecafa299d3fb5746ca972`  
		Last Modified: Sat, 10 Apr 2021 01:01:51 GMT  
		Size: 44.1 MB (44091992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab925f915ae26ca19efd38242f0b115eccef69b7a8277a6e88e02b45c0468ba7`  
		Last Modified: Sat, 10 Apr 2021 01:02:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:69cd967884c53bef7cdb1184d7880b661b23a67866e6df52e1fa9ff52570290f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38481737946a434f6ef73f479e91ee738069e225b798c4458571fe143beb2c20`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:02:42 GMT
ADD file:4c101c517b88a8d25a4997ab4d938ea50aaa265c7f88a4e63edaaed37d89a288 in / 
# Sat, 10 Apr 2021 01:02:43 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:02:51 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:533b099902e847172558070703785f6c70f0c6912fefcfd283f3b0e3ebc306c5`  
		Last Modified: Sat, 10 Apr 2021 01:10:12 GMT  
		Size: 42.1 MB (42120304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ec0eb29b8923418a3b0826f683d6e5298892fca802d7b8bfa3641b856b8a75`  
		Last Modified: Sat, 10 Apr 2021 01:10:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a86129813d2e48b657b29a64170c1b714f27c5cdd04404992011c204d0a3a128
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae88b3ad196c6ad22638b1b36259cf9fd6b42589798b93fec295b72ffb8ec2d5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:43:48 GMT
ADD file:64990d14743657dbcbe885739e43ac964a0239a63e4693e6401b0884ab96e09b in / 
# Sat, 10 Apr 2021 00:43:50 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:44:00 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:30bd672115ff6f225cb98d2d7f1ed62feb72c2612297b2ac615e762e436c64ec`  
		Last Modified: Sat, 10 Apr 2021 00:49:51 GMT  
		Size: 43.2 MB (43177772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5393252c8f2b2a82d38aed3862785e8af68ad45294d974c94b59233215170b14`  
		Last Modified: Sat, 10 Apr 2021 00:50:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:ae496d3b3660a75aa2d456b4b3fa5d081987e2734f6e5f24b21e5054676c7837
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee757184e56d20c9877f15ad641a74a2e7a9a71e8c9b5ce9c0dd8967f979325`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:14 GMT
ADD file:cebeeb1ed904e9433778c60c09ed31939334fd4f1c9550cce191b3bff4df0272 in / 
# Sat, 10 Apr 2021 00:41:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:41:21 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8270215e0f4bee2960e85333265840385530ee75e6f553f8cfc3e5b0534bf0e`  
		Last Modified: Sat, 10 Apr 2021 00:48:47 GMT  
		Size: 46.1 MB (46098724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0920ce87e624a5bf8409ac8c624dd91a5aec00c151cd18079924ef8c0055aa3e`  
		Last Modified: Sat, 10 Apr 2021 00:49:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
