## `debian:buster-backports`

```console
$ docker pull debian@sha256:81589c852a999a6a5fc35813b0fa6bfe00f26414eb0a42bf36108133a9652671
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:69144d60ca675c910e0e8efe0d405c4031620f86a2218c3855cf5c5e3f8fce59
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50396138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b4eaeb7691a4c549394d27fb241209061765bd7f4822a546e3b4ec115ff59a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:23:04 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800f673b4bb9d0d14a29f59f6f17ab4706ef284672a58da41a81a34825475eac`  
		Last Modified: Thu, 10 Sep 2020 00:33:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a1554cfdfa262912113ee42319a3395899bc0841f4587a43ae32963627cf493f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b88b66c96afbb1b3664651ae23450f30e679302f507031bd90baf8d409c059`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:21 GMT
ADD file:a4eb5b1dc9adb84c94eff31b2ba5949b13b32831aff9a39d23ba20bc76d16449 in / 
# Wed, 09 Sep 2020 23:53:24 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:53:33 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:246514107a0cb62099f20170639c25bf457998ef723200e2e9343b78321b1a79`  
		Last Modified: Thu, 10 Sep 2020 00:02:25 GMT  
		Size: 48.1 MB (48108877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f4970f8e182062a8f02aeb40732dc47fd730dab553350cfe27918ad082ec28`  
		Last Modified: Thu, 10 Sep 2020 00:02:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a7c1609f103f5746bca12c50d7a66056a3f78ae71e160c666463612f9bf0646a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45869482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecc0515703012c05a3a6df41638cf6d1ba4585c4835738f885a172cb3d33bbe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:02 GMT
ADD file:e03270d36cef8171f1f6303860ff31bb1c0eb10642b8173bfdfef9f77fa4f89c in / 
# Tue, 13 Oct 2020 00:59:04 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 00:59:12 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c0fdcca2cbb5e316a288f39c8c2006f45544568ea04623c036e0b1faa066bbe`  
		Last Modified: Tue, 13 Oct 2020 01:08:04 GMT  
		Size: 45.9 MB (45869258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15354e833c98818ca40fffceca5d5ec441462e230283fb2f13578d3b24328b77`  
		Last Modified: Tue, 13 Oct 2020 01:08:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bb8ad1527287fe6c206ecf2b90f638383a6106546fdbec6865376c4971d0f238
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49175773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703da69b5448aa6c8084b94742fa0a9a22224d2054ff04896346226ca84b40de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:21 GMT
ADD file:c8c11e622b1b8a1e31f32e2457ff4d1314d5cd4a7ad22b3991ab9d0542db23fd in / 
# Wed, 09 Sep 2020 23:50:22 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:50:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3a32671b6316bd11f4bf18cb034394ac94d2bb3bc6d09de388b19b06fb94b91`  
		Last Modified: Wed, 09 Sep 2020 23:58:45 GMT  
		Size: 49.2 MB (49175549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4646245b23148775491ff2e67dcd0eeb9ead2be242fbbdaa9694b22cbe05383d`  
		Last Modified: Wed, 09 Sep 2020 23:58:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:f74cc2af79a9462de38df83c113d83614478643472448a9d5e11c688613af537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51159075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf06d0576f5067edfc2e8905489b301ac0fb49b99b931e10d001bb3c81bd8c8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:58 GMT
ADD file:39c4b1e1e5d34f52ad1f95b26bfbbf45f307b94a52d472a561496c440f96d8a2 in / 
# Wed, 09 Sep 2020 23:39:59 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:40:05 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c89594b72f230eaccb7faa969906602c0f8e2667b7e30e66fe230243f1b5f1d0`  
		Last Modified: Wed, 09 Sep 2020 23:46:14 GMT  
		Size: 51.2 MB (51158853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4559b9909fae8e404b8269d09323920b95f6f888c0227c3bcbea11f8537fbd6a`  
		Last Modified: Wed, 09 Sep 2020 23:46:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:180bad8773608db923b0f066bb87a7fa5b6e1f381d92ee7a554b650a04330312
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49017418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08f955689e915af8684e6e83e2bb13c1d05fb286e42886ab6febe59884d577`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:09:23 GMT
ADD file:0ad6bbc90b50de1f5a0751fd1da65e211c687820c0339fdd38f12d689638b939 in / 
# Tue, 13 Oct 2020 01:09:24 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:09:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9fd0710976c57d8d2e5a2f13cccd726cca5d8b0f607868465c8cffbdcf2d3940`  
		Last Modified: Tue, 13 Oct 2020 01:15:56 GMT  
		Size: 49.0 MB (49017194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e94e4cad18944c267bee0e2c3e208382d0d689a18f037ce7c056ed67145b84`  
		Last Modified: Tue, 13 Oct 2020 01:16:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:83b5712737c0b840dae06cc377158fe4cf1ea347e467da036c0a0315853b015d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54142869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17712df69f307b8698a58eefd0cd3ae664068f274f396fb178a50246d9f1811c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:04:56 GMT
ADD file:a2329a0372b3b40ca345795d86a78ab4cdaa3a1eeda3a5ece35a83881543db1a in / 
# Thu, 10 Sep 2020 01:05:18 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:05:49 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aff7fe9e9819c2b9d4338fae03bd06eb6784016bcf53b2eeab88c21e47dea428`  
		Last Modified: Thu, 10 Sep 2020 01:26:27 GMT  
		Size: 54.1 MB (54142644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15431f54042ca83924753a2653a78b275bbe28e22ae8858f8ea198dc5f344b2`  
		Last Modified: Thu, 10 Sep 2020 01:26:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:64e56c2bc44faa8c1016efe7dc05bf2b9bd8caf1326645b95b7a745a72bb97d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48966516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab2f05fcb20949a7ffd9e6eb95c9073546a6880996c245b6e1b919acb3aa031`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:06 GMT
ADD file:cc8968c8733f7fb6fb644b948e4a21999440d079560afbb2acb9d666de3886ec in / 
# Tue, 13 Oct 2020 01:42:09 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dcbd85f88306d080bce94006a992947eaf462efa80b07c202b0514e6ef412fdf`  
		Last Modified: Tue, 13 Oct 2020 01:45:28 GMT  
		Size: 49.0 MB (48966292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4703c17627f8e28f2a0fec55542151e23b080b39a39d05bd7549ac60352b0103`  
		Last Modified: Tue, 13 Oct 2020 01:45:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
