<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20211201.0`](#amazonlinux20202112010)
-	[`amazonlinux:2.0.20211201.0-with-sources`](#amazonlinux20202112010-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20211201.0`](#amazonlinux2018030202112010)
-	[`amazonlinux:2018.03.0.20211201.0-with-sources`](#amazonlinux2018030202112010-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:8fd3b5a89223483bb8de4a3d06dcffe0c017f6ab7eef2b998ed4fc944b85f0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:84ec72c9c233e160a8e7771bd4d2e82bf876681a981f7162cd31c6e78fd102be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf363a0d66c88d9986750f056329dd36f2cd292d67c2e51c587dfe3e705d5cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Nov 2021 01:19:54 GMT
ADD file:2c36a545f5fd3a8e5b6ff9d03786a858cd6d3b54b1d5fc8062c022dd10c2c65b in / 
# Wed, 10 Nov 2021 01:19:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b3f2a98e30d17e42b896165da66f458ece941ec21b0cfc7f9870c31bc5811a8`  
		Last Modified: Wed, 10 Nov 2021 01:20:53 GMT  
		Size: 62.4 MB (62427664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:d29ed853f59846db64763649a1c1b4199e2f86620672babb819365207d35188f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7710b6d48450e71cb465ac60dae2bfbedba5b958659183455718b5591f2ca157
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515030566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71e39e9f123fb4b8e15e9bbb296390feebb890a80d02d97cf8594de7deb2bce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Nov 2021 01:19:54 GMT
ADD file:2c36a545f5fd3a8e5b6ff9d03786a858cd6d3b54b1d5fc8062c022dd10c2c65b in / 
# Wed, 10 Nov 2021 01:19:55 GMT
CMD ["/bin/bash"]
# Wed, 10 Nov 2021 01:20:22 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-27bb5888fce9879d31309d8630e620315bfd93c1fdae3bb011dd8b3d982994d3.tar.gz"  && echo "b46a06101fe9d6a4a72d6f21944ac448a6c55e7a5b76b26f6052cbc1b775a31c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:2b3f2a98e30d17e42b896165da66f458ece941ec21b0cfc7f9870c31bc5811a8`  
		Last Modified: Wed, 10 Nov 2021 01:20:53 GMT  
		Size: 62.4 MB (62427664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d84e9e4e6382e61b6c875897cebdd9a07a14ebe1e2f320fe1a1c5b5ecf08c`  
		Last Modified: Wed, 10 Nov 2021 01:21:26 GMT  
		Size: 452.6 MB (452602902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:d8b4ba4fa093ca879d3af505f5e2083c4cfb42df3e83abf7bfad12ed208d26d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:05295e83275444cae0e55601f6a545b548fd3e03e8ef9a4ab9c38a52071519b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61976108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99c40d6547efd6328851315f5bcf7e6a8e0a96c200583a445fc0cdcd2146b81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:7e9896533f552171f29da8eb550aa2ee4f430e7b9d4ec99206ab10aa0fa53804
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63692547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbac2e4cd8c610c103ed56f38ab52b37cda9101552f73e0fe69809ce710c7ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:89957b04113c0a228c234ec2b163c89ad3eaeaaf4ca2cf29e513f539c12105a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7270588a2f1d44b6515784c67c8887f7ae83def17069edd48910f555d7eda296
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543036131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acec5c4453b5b9e508505dc7ed855169c8df9f295df44f0cb767a4fa5d8ee71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 22:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e9fd3b1031f9a7540f8249e5d30e6439633e1eb09f394919e35ac5017ec18c93.tar.gz"  && echo "08179d9c712a9a7f501377be8ec5e1f7c229343a5bec655c93db62c623831c7c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9dd65b340056c10ece74bbe3f53f0a1ec019751a8d9b835573cac406fda501`  
		Last Modified: Thu, 21 Oct 2021 22:21:05 GMT  
		Size: 481.1 MB (481060023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f430c04ebeb56b96104035a268952662f973de96c4643d53f5ffc56fb8e1e4fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485506862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0843a85e5d33304d882cf4a230dcc700a1e35540601466316552791924470a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Thu, 02 Dec 2021 21:25:41 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-faddacaa94ce45cab3ebd75298e985ccc4100e074eae55e6692f4139b7719f13.tar.gz"  && echo "821fcdbe479764a7bf796e4f23a04df2ad960dc88f93f9dfb4492deb77ec6522  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2f71867fbb5d9040a4eeaff7f0e49f8cbb45e0b4a563c6f2a7d151c4cd47c`  
		Last Modified: Thu, 02 Dec 2021 21:26:51 GMT  
		Size: 421.8 MB (421814315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20211201.0`

```console
$ docker pull amazonlinux@sha256:0c0998e3c02de34671dbd04706aeaf8c5c7a4d331ffcf701598d2333bcece15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20211201.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:7e9896533f552171f29da8eb550aa2ee4f430e7b9d4ec99206ab10aa0fa53804
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63692547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbac2e4cd8c610c103ed56f38ab52b37cda9101552f73e0fe69809ce710c7ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20211201.0-with-sources`

```console
$ docker pull amazonlinux@sha256:d00121fa3f0e453acdea8a246bbd7da64e7a14e323442636130b6f1c07c8cba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20211201.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f430c04ebeb56b96104035a268952662f973de96c4643d53f5ffc56fb8e1e4fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485506862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0843a85e5d33304d882cf4a230dcc700a1e35540601466316552791924470a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Thu, 02 Dec 2021 21:25:41 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-faddacaa94ce45cab3ebd75298e985ccc4100e074eae55e6692f4139b7719f13.tar.gz"  && echo "821fcdbe479764a7bf796e4f23a04df2ad960dc88f93f9dfb4492deb77ec6522  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2f71867fbb5d9040a4eeaff7f0e49f8cbb45e0b4a563c6f2a7d151c4cd47c`  
		Last Modified: Thu, 02 Dec 2021 21:26:51 GMT  
		Size: 421.8 MB (421814315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:8fd3b5a89223483bb8de4a3d06dcffe0c017f6ab7eef2b998ed4fc944b85f0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:84ec72c9c233e160a8e7771bd4d2e82bf876681a981f7162cd31c6e78fd102be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf363a0d66c88d9986750f056329dd36f2cd292d67c2e51c587dfe3e705d5cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Nov 2021 01:19:54 GMT
ADD file:2c36a545f5fd3a8e5b6ff9d03786a858cd6d3b54b1d5fc8062c022dd10c2c65b in / 
# Wed, 10 Nov 2021 01:19:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b3f2a98e30d17e42b896165da66f458ece941ec21b0cfc7f9870c31bc5811a8`  
		Last Modified: Wed, 10 Nov 2021 01:20:53 GMT  
		Size: 62.4 MB (62427664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:d29ed853f59846db64763649a1c1b4199e2f86620672babb819365207d35188f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7710b6d48450e71cb465ac60dae2bfbedba5b958659183455718b5591f2ca157
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515030566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71e39e9f123fb4b8e15e9bbb296390feebb890a80d02d97cf8594de7deb2bce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Nov 2021 01:19:54 GMT
ADD file:2c36a545f5fd3a8e5b6ff9d03786a858cd6d3b54b1d5fc8062c022dd10c2c65b in / 
# Wed, 10 Nov 2021 01:19:55 GMT
CMD ["/bin/bash"]
# Wed, 10 Nov 2021 01:20:22 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-27bb5888fce9879d31309d8630e620315bfd93c1fdae3bb011dd8b3d982994d3.tar.gz"  && echo "b46a06101fe9d6a4a72d6f21944ac448a6c55e7a5b76b26f6052cbc1b775a31c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:2b3f2a98e30d17e42b896165da66f458ece941ec21b0cfc7f9870c31bc5811a8`  
		Last Modified: Wed, 10 Nov 2021 01:20:53 GMT  
		Size: 62.4 MB (62427664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d84e9e4e6382e61b6c875897cebdd9a07a14ebe1e2f320fe1a1c5b5ecf08c`  
		Last Modified: Wed, 10 Nov 2021 01:21:26 GMT  
		Size: 452.6 MB (452602902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20211201.0`

```console
$ docker pull amazonlinux@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `amazonlinux:2018.03.0.20211201.0-with-sources`

```console
$ docker pull amazonlinux@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:d8b4ba4fa093ca879d3af505f5e2083c4cfb42df3e83abf7bfad12ed208d26d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:05295e83275444cae0e55601f6a545b548fd3e03e8ef9a4ab9c38a52071519b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61976108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99c40d6547efd6328851315f5bcf7e6a8e0a96c200583a445fc0cdcd2146b81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:7e9896533f552171f29da8eb550aa2ee4f430e7b9d4ec99206ab10aa0fa53804
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63692547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbac2e4cd8c610c103ed56f38ab52b37cda9101552f73e0fe69809ce710c7ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:89957b04113c0a228c234ec2b163c89ad3eaeaaf4ca2cf29e513f539c12105a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7270588a2f1d44b6515784c67c8887f7ae83def17069edd48910f555d7eda296
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543036131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acec5c4453b5b9e508505dc7ed855169c8df9f295df44f0cb767a4fa5d8ee71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 22:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e9fd3b1031f9a7540f8249e5d30e6439633e1eb09f394919e35ac5017ec18c93.tar.gz"  && echo "08179d9c712a9a7f501377be8ec5e1f7c229343a5bec655c93db62c623831c7c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9dd65b340056c10ece74bbe3f53f0a1ec019751a8d9b835573cac406fda501`  
		Last Modified: Thu, 21 Oct 2021 22:21:05 GMT  
		Size: 481.1 MB (481060023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f430c04ebeb56b96104035a268952662f973de96c4643d53f5ffc56fb8e1e4fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485506862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0843a85e5d33304d882cf4a230dcc700a1e35540601466316552791924470a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Thu, 02 Dec 2021 21:25:41 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-faddacaa94ce45cab3ebd75298e985ccc4100e074eae55e6692f4139b7719f13.tar.gz"  && echo "821fcdbe479764a7bf796e4f23a04df2ad960dc88f93f9dfb4492deb77ec6522  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2f71867fbb5d9040a4eeaff7f0e49f8cbb45e0b4a563c6f2a7d151c4cd47c`  
		Last Modified: Thu, 02 Dec 2021 21:26:51 GMT  
		Size: 421.8 MB (421814315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
