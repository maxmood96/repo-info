<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20221103.3`](#amazonlinux20202211033)
-	[`amazonlinux:2.0.20221103.3-with-sources`](#amazonlinux20202211033-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20221018.0`](#amazonlinux2018030202210180)
-	[`amazonlinux:2018.03.0.20221018.0-with-sources`](#amazonlinux2018030202210180-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20221101.0`](#amazonlinux20220202211010)
-	[`amazonlinux:2022.0.20221101.0-with-sources`](#amazonlinux20220202211010-with-sources)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:devel-with-sources`](#amazonlinuxdevel-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:eb90fa0fd56cf880979f65bea71c7eb281c7dc89a488d7092ead33d2b9b2e46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e8df9dda3c5292dd7ef9a88d4f48f137777d10a66a5092c1fcca487e68f9d646
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62313541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5363925e500c1013b0ec6e6b7a360d9c5fce273cdde1c66cfbe207d2331e59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Nov 2022 00:20:14 GMT
ADD file:0410dbf81388508f909ade34c62fad7fec8bf5bab19b58a8a35c41acee8b4740 in / 
# Wed, 09 Nov 2022 00:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:239d83e9c6fb7a202ec4084ddd8523b8c6adecb0018abbeb8e5527303640c8d9`  
		Last Modified: Wed, 09 Nov 2022 00:21:28 GMT  
		Size: 62.3 MB (62313541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:645b31167fc038f0e7adcdf2ff61ade80b5196df1b28db447dd60d837e963062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e16ebcdcc59bbaec60b9d8a84b0268f293bfd4a937be37c2ac2c1bbd2d851bbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515019772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbce77f59d1e6d589eafa0793b60aa0bb0b16dd1eec9459f1c2dd975d4e7ef69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Nov 2022 00:20:14 GMT
ADD file:0410dbf81388508f909ade34c62fad7fec8bf5bab19b58a8a35c41acee8b4740 in / 
# Wed, 09 Nov 2022 00:20:14 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 00:20:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6187381cfff74a5e739858bf043ff837ea10f446423f99fdb7c9af84c17343a2.tar.gz"     && echo "48bbea24b4a488fe06936dd9651cde99e66dc16ee4c06feaa246edc9393c1cb5  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:239d83e9c6fb7a202ec4084ddd8523b8c6adecb0018abbeb8e5527303640c8d9`  
		Last Modified: Wed, 09 Nov 2022 00:21:28 GMT  
		Size: 62.3 MB (62313541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140305c0ab9b02db4b457cd8851da53989035af98c8c9e145649884d289b9faa`  
		Last Modified: Wed, 09 Nov 2022 00:21:58 GMT  
		Size: 452.7 MB (452706231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:a8e94ea6c17f7749b1beb0ac2c3245e0b99804190f31e05f68a0fabb5bea1787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0eefa899a816bf75b072f1c002a9a6d620d2cde73983fee2380533571eb99d20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62262225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e809582795f51280dda491769531ca101af7ce73ff67ec039597b1f000fef8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6ed3f8651e7e6ae661e3bdac75a80bc532ac90dfae8ce303d866caae3b60b980
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63867424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c3d5a14ae516d5edaa98abdd502ef3e1387825976894b400cc5e28c05c9f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:82a38eba9fec67c342b9087ac546046c2c9c7fbc0f2b095ea66b328c5f0da577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3b2577f41f953dbcdf5048d7758ba6ea256d969bcedaec5c55c51e8f0a6ed33e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.5 MB (486483327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d07e7f0e1d5c7174795d3bdf891ba42e57a9fc86901abb1f756e42be2634ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:33:01 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-492ef4bbb2a8bda50ad4bc02c89770eeaa7296d257948debf28ef46507bcc438.tar.gz"     && echo "db09c810ec34c11f75ae846626c059edfd084bc81f0f768ccceae965e1866cff  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c299c6bd3174bbd956c64ed7b2293797f088630f99cf594aa56ff9ce455d`  
		Last Modified: Thu, 17 Nov 2022 01:34:09 GMT  
		Size: 424.2 MB (424221102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:a275540bb68d0bc1ba9f805584cfb26e70b947abdd235480fa30d649ac9b1d07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488088520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f200fd70b2c39be62241a71382721998d2e259d3f8b519ff77d9528292774e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:39:45 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-492ef4bbb2a8bda50ad4bc02c89770eeaa7296d257948debf28ef46507bcc438.tar.gz"     && echo "db09c810ec34c11f75ae846626c059edfd084bc81f0f768ccceae965e1866cff  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86c33f2344f55ce165a1f4a0d676258f7c17051b624ebf27aef2b227c95f4cc`  
		Last Modified: Thu, 17 Nov 2022 01:40:44 GMT  
		Size: 424.2 MB (424221096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20221103.3`

```console
$ docker pull amazonlinux@sha256:a8e94ea6c17f7749b1beb0ac2c3245e0b99804190f31e05f68a0fabb5bea1787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20221103.3` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0eefa899a816bf75b072f1c002a9a6d620d2cde73983fee2380533571eb99d20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62262225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e809582795f51280dda491769531ca101af7ce73ff67ec039597b1f000fef8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20221103.3` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6ed3f8651e7e6ae661e3bdac75a80bc532ac90dfae8ce303d866caae3b60b980
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63867424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c3d5a14ae516d5edaa98abdd502ef3e1387825976894b400cc5e28c05c9f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20221103.3-with-sources`

```console
$ docker pull amazonlinux@sha256:82a38eba9fec67c342b9087ac546046c2c9c7fbc0f2b095ea66b328c5f0da577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20221103.3-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3b2577f41f953dbcdf5048d7758ba6ea256d969bcedaec5c55c51e8f0a6ed33e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.5 MB (486483327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d07e7f0e1d5c7174795d3bdf891ba42e57a9fc86901abb1f756e42be2634ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:33:01 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-492ef4bbb2a8bda50ad4bc02c89770eeaa7296d257948debf28ef46507bcc438.tar.gz"     && echo "db09c810ec34c11f75ae846626c059edfd084bc81f0f768ccceae965e1866cff  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c299c6bd3174bbd956c64ed7b2293797f088630f99cf594aa56ff9ce455d`  
		Last Modified: Thu, 17 Nov 2022 01:34:09 GMT  
		Size: 424.2 MB (424221102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20221103.3-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:a275540bb68d0bc1ba9f805584cfb26e70b947abdd235480fa30d649ac9b1d07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488088520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f200fd70b2c39be62241a71382721998d2e259d3f8b519ff77d9528292774e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:39:45 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-492ef4bbb2a8bda50ad4bc02c89770eeaa7296d257948debf28ef46507bcc438.tar.gz"     && echo "db09c810ec34c11f75ae846626c059edfd084bc81f0f768ccceae965e1866cff  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86c33f2344f55ce165a1f4a0d676258f7c17051b624ebf27aef2b227c95f4cc`  
		Last Modified: Thu, 17 Nov 2022 01:40:44 GMT  
		Size: 424.2 MB (424221096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:eb90fa0fd56cf880979f65bea71c7eb281c7dc89a488d7092ead33d2b9b2e46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e8df9dda3c5292dd7ef9a88d4f48f137777d10a66a5092c1fcca487e68f9d646
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62313541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5363925e500c1013b0ec6e6b7a360d9c5fce273cdde1c66cfbe207d2331e59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Nov 2022 00:20:14 GMT
ADD file:0410dbf81388508f909ade34c62fad7fec8bf5bab19b58a8a35c41acee8b4740 in / 
# Wed, 09 Nov 2022 00:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:239d83e9c6fb7a202ec4084ddd8523b8c6adecb0018abbeb8e5527303640c8d9`  
		Last Modified: Wed, 09 Nov 2022 00:21:28 GMT  
		Size: 62.3 MB (62313541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:645b31167fc038f0e7adcdf2ff61ade80b5196df1b28db447dd60d837e963062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e16ebcdcc59bbaec60b9d8a84b0268f293bfd4a937be37c2ac2c1bbd2d851bbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515019772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbce77f59d1e6d589eafa0793b60aa0bb0b16dd1eec9459f1c2dd975d4e7ef69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Nov 2022 00:20:14 GMT
ADD file:0410dbf81388508f909ade34c62fad7fec8bf5bab19b58a8a35c41acee8b4740 in / 
# Wed, 09 Nov 2022 00:20:14 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 00:20:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6187381cfff74a5e739858bf043ff837ea10f446423f99fdb7c9af84c17343a2.tar.gz"     && echo "48bbea24b4a488fe06936dd9651cde99e66dc16ee4c06feaa246edc9393c1cb5  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:239d83e9c6fb7a202ec4084ddd8523b8c6adecb0018abbeb8e5527303640c8d9`  
		Last Modified: Wed, 09 Nov 2022 00:21:28 GMT  
		Size: 62.3 MB (62313541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140305c0ab9b02db4b457cd8851da53989035af98c8c9e145649884d289b9faa`  
		Last Modified: Wed, 09 Nov 2022 00:21:58 GMT  
		Size: 452.7 MB (452706231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20221018.0`

```console
$ docker pull amazonlinux@sha256:eb90fa0fd56cf880979f65bea71c7eb281c7dc89a488d7092ead33d2b9b2e46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20221018.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e8df9dda3c5292dd7ef9a88d4f48f137777d10a66a5092c1fcca487e68f9d646
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62313541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5363925e500c1013b0ec6e6b7a360d9c5fce273cdde1c66cfbe207d2331e59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Nov 2022 00:20:14 GMT
ADD file:0410dbf81388508f909ade34c62fad7fec8bf5bab19b58a8a35c41acee8b4740 in / 
# Wed, 09 Nov 2022 00:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:239d83e9c6fb7a202ec4084ddd8523b8c6adecb0018abbeb8e5527303640c8d9`  
		Last Modified: Wed, 09 Nov 2022 00:21:28 GMT  
		Size: 62.3 MB (62313541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20221018.0-with-sources`

```console
$ docker pull amazonlinux@sha256:645b31167fc038f0e7adcdf2ff61ade80b5196df1b28db447dd60d837e963062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20221018.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e16ebcdcc59bbaec60b9d8a84b0268f293bfd4a937be37c2ac2c1bbd2d851bbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515019772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbce77f59d1e6d589eafa0793b60aa0bb0b16dd1eec9459f1c2dd975d4e7ef69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 09 Nov 2022 00:20:14 GMT
ADD file:0410dbf81388508f909ade34c62fad7fec8bf5bab19b58a8a35c41acee8b4740 in / 
# Wed, 09 Nov 2022 00:20:14 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 00:20:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6187381cfff74a5e739858bf043ff837ea10f446423f99fdb7c9af84c17343a2.tar.gz"     && echo "48bbea24b4a488fe06936dd9651cde99e66dc16ee4c06feaa246edc9393c1cb5  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:239d83e9c6fb7a202ec4084ddd8523b8c6adecb0018abbeb8e5527303640c8d9`  
		Last Modified: Wed, 09 Nov 2022 00:21:28 GMT  
		Size: 62.3 MB (62313541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140305c0ab9b02db4b457cd8851da53989035af98c8c9e145649884d289b9faa`  
		Last Modified: Wed, 09 Nov 2022 00:21:58 GMT  
		Size: 452.7 MB (452706231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022`

```console
$ docker pull amazonlinux@sha256:98501b204b89ad4b5eb08ab06f2f7f82edc3fa637ba61ab4015d8b0856865b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:21e0ad332ee2c3723b20357f76829cda81da6ff6e2630eed6c56658514a75cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57657867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76310d45eddd6a35aab56db52088c8936e5507e2028d51b07da7ecc0ddebf42c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:4ef67a181bdcff39e952bb9251c0a2ffeef76b11a8f97e4a6f9fb8d9cf135136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56505867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d88c9fe91d0f351545f815433c3beb52cff87f1686557df9eec87f4e4acdf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:b929906fa10216314b0f1e2dc978a65b9874c515479c0651bcbd4728afb4ad8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:47b2413f80d9392dbbdabb09d40ede432afd8dc11a638cc2176c8f4399ad3f87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.8 MB (387791955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419b95c0aecedd809286c2f73a221ceed144a188f5ee55079c1cef975eba20a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Nov 2022 23:11:43 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9017832186b37ba807d501395b1ecd1dee072363f2dbf07cd660b9c6901e23d5.tar.gz"     && echo "e381f621dad069a24ac99c48de67decd4a83465925c195fd186bb3ed587d7a9c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfa8588296ea9cc5617b6ef566ee485a036bd55235e0d28bec7633d17a17f42`  
		Last Modified: Tue, 01 Nov 2022 23:12:44 GMT  
		Size: 330.1 MB (330134088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6468c6cf7df684bb1ae74c398a80f81752d6683e98006549905dc511018e6dbd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386639956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bcdcbc0090700ece3f1f96dee45ce818350cf95282dd1d4f08f0f1d47d55d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
# Tue, 01 Nov 2022 23:11:32 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9017832186b37ba807d501395b1ecd1dee072363f2dbf07cd660b9c6901e23d5.tar.gz"     && echo "e381f621dad069a24ac99c48de67decd4a83465925c195fd186bb3ed587d7a9c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e1358755b392436e218dd02e545f2712370f5328f9d4542512845f4059fc5b`  
		Last Modified: Tue, 01 Nov 2022 23:12:28 GMT  
		Size: 330.1 MB (330134089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20221101.0`

```console
$ docker pull amazonlinux@sha256:98501b204b89ad4b5eb08ab06f2f7f82edc3fa637ba61ab4015d8b0856865b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20221101.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:21e0ad332ee2c3723b20357f76829cda81da6ff6e2630eed6c56658514a75cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57657867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76310d45eddd6a35aab56db52088c8936e5507e2028d51b07da7ecc0ddebf42c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20221101.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:4ef67a181bdcff39e952bb9251c0a2ffeef76b11a8f97e4a6f9fb8d9cf135136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56505867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d88c9fe91d0f351545f815433c3beb52cff87f1686557df9eec87f4e4acdf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20221101.0-with-sources`

```console
$ docker pull amazonlinux@sha256:b929906fa10216314b0f1e2dc978a65b9874c515479c0651bcbd4728afb4ad8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20221101.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:47b2413f80d9392dbbdabb09d40ede432afd8dc11a638cc2176c8f4399ad3f87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.8 MB (387791955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419b95c0aecedd809286c2f73a221ceed144a188f5ee55079c1cef975eba20a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Nov 2022 23:11:43 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9017832186b37ba807d501395b1ecd1dee072363f2dbf07cd660b9c6901e23d5.tar.gz"     && echo "e381f621dad069a24ac99c48de67decd4a83465925c195fd186bb3ed587d7a9c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfa8588296ea9cc5617b6ef566ee485a036bd55235e0d28bec7633d17a17f42`  
		Last Modified: Tue, 01 Nov 2022 23:12:44 GMT  
		Size: 330.1 MB (330134088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20221101.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6468c6cf7df684bb1ae74c398a80f81752d6683e98006549905dc511018e6dbd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386639956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bcdcbc0090700ece3f1f96dee45ce818350cf95282dd1d4f08f0f1d47d55d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
# Tue, 01 Nov 2022 23:11:32 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9017832186b37ba807d501395b1ecd1dee072363f2dbf07cd660b9c6901e23d5.tar.gz"     && echo "e381f621dad069a24ac99c48de67decd4a83465925c195fd186bb3ed587d7a9c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e1358755b392436e218dd02e545f2712370f5328f9d4542512845f4059fc5b`  
		Last Modified: Tue, 01 Nov 2022 23:12:28 GMT  
		Size: 330.1 MB (330134089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:98501b204b89ad4b5eb08ab06f2f7f82edc3fa637ba61ab4015d8b0856865b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:21e0ad332ee2c3723b20357f76829cda81da6ff6e2630eed6c56658514a75cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57657867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76310d45eddd6a35aab56db52088c8936e5507e2028d51b07da7ecc0ddebf42c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:4ef67a181bdcff39e952bb9251c0a2ffeef76b11a8f97e4a6f9fb8d9cf135136
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56505867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d88c9fe91d0f351545f815433c3beb52cff87f1686557df9eec87f4e4acdf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:b929906fa10216314b0f1e2dc978a65b9874c515479c0651bcbd4728afb4ad8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:47b2413f80d9392dbbdabb09d40ede432afd8dc11a638cc2176c8f4399ad3f87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.8 MB (387791955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419b95c0aecedd809286c2f73a221ceed144a188f5ee55079c1cef975eba20a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Nov 2022 23:11:43 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9017832186b37ba807d501395b1ecd1dee072363f2dbf07cd660b9c6901e23d5.tar.gz"     && echo "e381f621dad069a24ac99c48de67decd4a83465925c195fd186bb3ed587d7a9c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfa8588296ea9cc5617b6ef566ee485a036bd55235e0d28bec7633d17a17f42`  
		Last Modified: Tue, 01 Nov 2022 23:12:44 GMT  
		Size: 330.1 MB (330134088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6468c6cf7df684bb1ae74c398a80f81752d6683e98006549905dc511018e6dbd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386639956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bcdcbc0090700ece3f1f96dee45ce818350cf95282dd1d4f08f0f1d47d55d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
# Tue, 01 Nov 2022 23:11:32 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9017832186b37ba807d501395b1ecd1dee072363f2dbf07cd660b9c6901e23d5.tar.gz"     && echo "e381f621dad069a24ac99c48de67decd4a83465925c195fd186bb3ed587d7a9c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e1358755b392436e218dd02e545f2712370f5328f9d4542512845f4059fc5b`  
		Last Modified: Tue, 01 Nov 2022 23:12:28 GMT  
		Size: 330.1 MB (330134089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:a8e94ea6c17f7749b1beb0ac2c3245e0b99804190f31e05f68a0fabb5bea1787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0eefa899a816bf75b072f1c002a9a6d620d2cde73983fee2380533571eb99d20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62262225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e809582795f51280dda491769531ca101af7ce73ff67ec039597b1f000fef8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6ed3f8651e7e6ae661e3bdac75a80bc532ac90dfae8ce303d866caae3b60b980
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63867424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c3d5a14ae516d5edaa98abdd502ef3e1387825976894b400cc5e28c05c9f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:82a38eba9fec67c342b9087ac546046c2c9c7fbc0f2b095ea66b328c5f0da577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3b2577f41f953dbcdf5048d7758ba6ea256d969bcedaec5c55c51e8f0a6ed33e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.5 MB (486483327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d07e7f0e1d5c7174795d3bdf891ba42e57a9fc86901abb1f756e42be2634ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:33:01 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-492ef4bbb2a8bda50ad4bc02c89770eeaa7296d257948debf28ef46507bcc438.tar.gz"     && echo "db09c810ec34c11f75ae846626c059edfd084bc81f0f768ccceae965e1866cff  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c299c6bd3174bbd956c64ed7b2293797f088630f99cf594aa56ff9ce455d`  
		Last Modified: Thu, 17 Nov 2022 01:34:09 GMT  
		Size: 424.2 MB (424221102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:a275540bb68d0bc1ba9f805584cfb26e70b947abdd235480fa30d649ac9b1d07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488088520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f200fd70b2c39be62241a71382721998d2e259d3f8b519ff77d9528292774e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:39:45 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-492ef4bbb2a8bda50ad4bc02c89770eeaa7296d257948debf28ef46507bcc438.tar.gz"     && echo "db09c810ec34c11f75ae846626c059edfd084bc81f0f768ccceae965e1866cff  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86c33f2344f55ce165a1f4a0d676258f7c17051b624ebf27aef2b227c95f4cc`  
		Last Modified: Thu, 17 Nov 2022 01:40:44 GMT  
		Size: 424.2 MB (424221096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
