<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20210813.1`](#amazonlinux20202108131)
-	[`amazonlinux:2.0.20210813.1-with-sources`](#amazonlinux20202108131-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20210721.0`](#amazonlinux2018030202107210)
-	[`amazonlinux:2018.03.0.20210721.0-with-sources`](#amazonlinux2018030202107210-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:d27370314abb4389b76dabe6721f034dd141e990168ce134f6769b111fcb3bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:42daf1b227ae9fe6dd053320b910d659926fadc02f348b65b9cb182bc79acd37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62447851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c591bfdb12c884bc1ff404b567bca8751f467d48442239f65ab63a1e18552e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:20:15 GMT
ADD file:4b16f85f418eaa2dc5061f87bad84182ff9a0908cae737752f418c8ee3b9fa50 in / 
# Mon, 02 Aug 2021 23:20:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:09b6f0cc07c54d7b46e1b5e0ada4bdd9506bec2fae181bc9715d654a48e750e4`  
		Last Modified: Mon, 02 Aug 2021 23:21:59 GMT  
		Size: 62.4 MB (62447851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:98883e114fdf3647d220fc3c13c820136d054972f7debfda13bb42bea93b58c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:faf1c1f381376b16dba4bb6422f7d66657306dcb2c5e3726e0f76c4e4d2a4d9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515035249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecef2b71e30d2675a113d05960cbcbe07f2fd2cf2b6eb0d9e8bc9f39aa9cf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:20:15 GMT
ADD file:4b16f85f418eaa2dc5061f87bad84182ff9a0908cae737752f418c8ee3b9fa50 in / 
# Mon, 02 Aug 2021 23:20:16 GMT
CMD ["/bin/bash"]
# Mon, 02 Aug 2021 23:20:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-96900e11bba57b06a0616a0bb6faa31e2d768b29001d11fdfa65375353e22e14.tar.gz"  && echo "a7a8bd81dd43de9a5705d1c943c0fb3dac49c485a21cd198a445164eab8a7b02  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:09b6f0cc07c54d7b46e1b5e0ada4bdd9506bec2fae181bc9715d654a48e750e4`  
		Last Modified: Mon, 02 Aug 2021 23:21:59 GMT  
		Size: 62.4 MB (62447851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b693288ab0a22247e28a2e046ea9615b796e0f7e85c4e690f029ac7aa0b3d`  
		Last Modified: Mon, 02 Aug 2021 23:22:28 GMT  
		Size: 452.6 MB (452587398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:1928c652007d27f087f43e3d652b51415b6751a10d522593166946f110a3be39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:634f9178bcf992c1f5d6fb15039f6fcc0de964c95988e2580ca768c5ccb70d61
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62000303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd1ba512ef19980b111b3142b816f1c6ecaa40c97f1f559e5ff7d39516b2201`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:dbe23db1df23ece9379b01227a4c3d0c1172c0e110b33e2ff205f0813404a4d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63430802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc885ab1197ab92e49001ef6bb3c07ed1e647e74001eb246449d1b63dd290f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:c82586d9cb52d1d76cf3fbb2ea919f57c4b2629d6ea200be46d808d6bd7d4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:dce35a75aef0b93ffd23eb89ef29cbcfa8a5619afccb1aa46f14ad45608023bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543005154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b21ebc73b4f0ad426d2078d98bd125c2ca49c25d9b59e7ceb804893910eff6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:20:29 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42305a36d448792755e5af8dfbd0d1038b87bb46a0541aa94586427d6f7deb2`  
		Last Modified: Thu, 09 Sep 2021 00:21:34 GMT  
		Size: 481.0 MB (481004851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:8fc64668ec668d7b6feeda33c34f5856a7cea21f35c5e886cf23d3bfc83b8451
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544435646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f59ebcd6e79e41e62d3e8568784dfb20b42bf78cf10ea0c4ed494a7bbe1d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:40:26 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df0eb3aed5c223e4cbf8c3710d58ea2ba788703f9f1a37ea6a2fe77ae50bdff`  
		Last Modified: Thu, 09 Sep 2021 00:41:45 GMT  
		Size: 481.0 MB (481004844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210813.1`

```console
$ docker pull amazonlinux@sha256:1928c652007d27f087f43e3d652b51415b6751a10d522593166946f110a3be39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210813.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:634f9178bcf992c1f5d6fb15039f6fcc0de964c95988e2580ca768c5ccb70d61
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62000303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd1ba512ef19980b111b3142b816f1c6ecaa40c97f1f559e5ff7d39516b2201`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210813.1` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:dbe23db1df23ece9379b01227a4c3d0c1172c0e110b33e2ff205f0813404a4d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63430802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc885ab1197ab92e49001ef6bb3c07ed1e647e74001eb246449d1b63dd290f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210813.1-with-sources`

```console
$ docker pull amazonlinux@sha256:c82586d9cb52d1d76cf3fbb2ea919f57c4b2629d6ea200be46d808d6bd7d4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210813.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:dce35a75aef0b93ffd23eb89ef29cbcfa8a5619afccb1aa46f14ad45608023bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543005154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b21ebc73b4f0ad426d2078d98bd125c2ca49c25d9b59e7ceb804893910eff6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:20:29 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42305a36d448792755e5af8dfbd0d1038b87bb46a0541aa94586427d6f7deb2`  
		Last Modified: Thu, 09 Sep 2021 00:21:34 GMT  
		Size: 481.0 MB (481004851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210813.1-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:8fc64668ec668d7b6feeda33c34f5856a7cea21f35c5e886cf23d3bfc83b8451
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544435646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f59ebcd6e79e41e62d3e8568784dfb20b42bf78cf10ea0c4ed494a7bbe1d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:40:26 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df0eb3aed5c223e4cbf8c3710d58ea2ba788703f9f1a37ea6a2fe77ae50bdff`  
		Last Modified: Thu, 09 Sep 2021 00:41:45 GMT  
		Size: 481.0 MB (481004844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:d27370314abb4389b76dabe6721f034dd141e990168ce134f6769b111fcb3bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:42daf1b227ae9fe6dd053320b910d659926fadc02f348b65b9cb182bc79acd37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62447851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c591bfdb12c884bc1ff404b567bca8751f467d48442239f65ab63a1e18552e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:20:15 GMT
ADD file:4b16f85f418eaa2dc5061f87bad84182ff9a0908cae737752f418c8ee3b9fa50 in / 
# Mon, 02 Aug 2021 23:20:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:09b6f0cc07c54d7b46e1b5e0ada4bdd9506bec2fae181bc9715d654a48e750e4`  
		Last Modified: Mon, 02 Aug 2021 23:21:59 GMT  
		Size: 62.4 MB (62447851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:98883e114fdf3647d220fc3c13c820136d054972f7debfda13bb42bea93b58c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:faf1c1f381376b16dba4bb6422f7d66657306dcb2c5e3726e0f76c4e4d2a4d9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515035249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecef2b71e30d2675a113d05960cbcbe07f2fd2cf2b6eb0d9e8bc9f39aa9cf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:20:15 GMT
ADD file:4b16f85f418eaa2dc5061f87bad84182ff9a0908cae737752f418c8ee3b9fa50 in / 
# Mon, 02 Aug 2021 23:20:16 GMT
CMD ["/bin/bash"]
# Mon, 02 Aug 2021 23:20:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-96900e11bba57b06a0616a0bb6faa31e2d768b29001d11fdfa65375353e22e14.tar.gz"  && echo "a7a8bd81dd43de9a5705d1c943c0fb3dac49c485a21cd198a445164eab8a7b02  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:09b6f0cc07c54d7b46e1b5e0ada4bdd9506bec2fae181bc9715d654a48e750e4`  
		Last Modified: Mon, 02 Aug 2021 23:21:59 GMT  
		Size: 62.4 MB (62447851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b693288ab0a22247e28a2e046ea9615b796e0f7e85c4e690f029ac7aa0b3d`  
		Last Modified: Mon, 02 Aug 2021 23:22:28 GMT  
		Size: 452.6 MB (452587398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210721.0`

```console
$ docker pull amazonlinux@sha256:d27370314abb4389b76dabe6721f034dd141e990168ce134f6769b111fcb3bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20210721.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:42daf1b227ae9fe6dd053320b910d659926fadc02f348b65b9cb182bc79acd37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62447851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c591bfdb12c884bc1ff404b567bca8751f467d48442239f65ab63a1e18552e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:20:15 GMT
ADD file:4b16f85f418eaa2dc5061f87bad84182ff9a0908cae737752f418c8ee3b9fa50 in / 
# Mon, 02 Aug 2021 23:20:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:09b6f0cc07c54d7b46e1b5e0ada4bdd9506bec2fae181bc9715d654a48e750e4`  
		Last Modified: Mon, 02 Aug 2021 23:21:59 GMT  
		Size: 62.4 MB (62447851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210721.0-with-sources`

```console
$ docker pull amazonlinux@sha256:98883e114fdf3647d220fc3c13c820136d054972f7debfda13bb42bea93b58c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20210721.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:faf1c1f381376b16dba4bb6422f7d66657306dcb2c5e3726e0f76c4e4d2a4d9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515035249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ecef2b71e30d2675a113d05960cbcbe07f2fd2cf2b6eb0d9e8bc9f39aa9cf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:20:15 GMT
ADD file:4b16f85f418eaa2dc5061f87bad84182ff9a0908cae737752f418c8ee3b9fa50 in / 
# Mon, 02 Aug 2021 23:20:16 GMT
CMD ["/bin/bash"]
# Mon, 02 Aug 2021 23:20:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-96900e11bba57b06a0616a0bb6faa31e2d768b29001d11fdfa65375353e22e14.tar.gz"  && echo "a7a8bd81dd43de9a5705d1c943c0fb3dac49c485a21cd198a445164eab8a7b02  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:09b6f0cc07c54d7b46e1b5e0ada4bdd9506bec2fae181bc9715d654a48e750e4`  
		Last Modified: Mon, 02 Aug 2021 23:21:59 GMT  
		Size: 62.4 MB (62447851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b693288ab0a22247e28a2e046ea9615b796e0f7e85c4e690f029ac7aa0b3d`  
		Last Modified: Mon, 02 Aug 2021 23:22:28 GMT  
		Size: 452.6 MB (452587398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:1928c652007d27f087f43e3d652b51415b6751a10d522593166946f110a3be39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:634f9178bcf992c1f5d6fb15039f6fcc0de964c95988e2580ca768c5ccb70d61
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62000303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd1ba512ef19980b111b3142b816f1c6ecaa40c97f1f559e5ff7d39516b2201`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:dbe23db1df23ece9379b01227a4c3d0c1172c0e110b33e2ff205f0813404a4d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63430802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc885ab1197ab92e49001ef6bb3c07ed1e647e74001eb246449d1b63dd290f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:c82586d9cb52d1d76cf3fbb2ea919f57c4b2629d6ea200be46d808d6bd7d4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:dce35a75aef0b93ffd23eb89ef29cbcfa8a5619afccb1aa46f14ad45608023bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543005154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b21ebc73b4f0ad426d2078d98bd125c2ca49c25d9b59e7ceb804893910eff6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:20:29 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42305a36d448792755e5af8dfbd0d1038b87bb46a0541aa94586427d6f7deb2`  
		Last Modified: Thu, 09 Sep 2021 00:21:34 GMT  
		Size: 481.0 MB (481004851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:8fc64668ec668d7b6feeda33c34f5856a7cea21f35c5e886cf23d3bfc83b8451
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544435646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f59ebcd6e79e41e62d3e8568784dfb20b42bf78cf10ea0c4ed494a7bbe1d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:40:26 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df0eb3aed5c223e4cbf8c3710d58ea2ba788703f9f1a37ea6a2fe77ae50bdff`  
		Last Modified: Thu, 09 Sep 2021 00:41:45 GMT  
		Size: 481.0 MB (481004844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
