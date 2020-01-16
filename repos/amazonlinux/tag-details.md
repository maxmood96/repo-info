<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03.0.20191219.0`](#amazonlinux2018030201912190)
-	[`amazonlinux:2018.03.0.20191219.0-with-sources`](#amazonlinux2018030201912190-with-sources)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2.0.20191217.0`](#amazonlinux20201912170)
-	[`amazonlinux:2.0.20191217.0-with-sources`](#amazonlinux20201912170-with-sources)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:5ded99e84532e28bbcf5ad466aeddc54eca2622a21e6f393cc6469c6ca8b1d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2e02adc1f2114a6efea2c06ba99c90ad3d5028d6c782c1210217204aa6f2aa9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62152740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1f3d6c1c4519a5ebb30495a78988409b2a8ffe4f06b1e620fa48b200f217d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 22 Oct 2019 01:29:16 GMT
ADD file:4a60739abc789db5501d860d9d7f1ccaa4b9a062c2f77adc7620d26b9331a4ad in / 
# Tue, 22 Oct 2019 01:29:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a94ca19f706b0fae65365af76666c91188cb9f6b7a6548a162179b4e34124d53`  
		Last Modified: Tue, 22 Oct 2019 01:30:58 GMT  
		Size: 62.2 MB (62152740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:292f57784050dc780d7ce9660795fa17204a03062c19d761ab958d28901ba63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e7562fd6a35798d6b003775bb0a2fb0c026e6433dd768d7fc3284bd900f603db
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387079952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4907fefc006913ec52f7d599f5b27afe493ac2a55e5b6ca1b8c9de838275929`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 22 Oct 2019 01:29:16 GMT
ADD file:4a60739abc789db5501d860d9d7f1ccaa4b9a062c2f77adc7620d26b9331a4ad in / 
# Tue, 22 Oct 2019 01:29:16 GMT
CMD ["/bin/bash"]
# Tue, 22 Oct 2019 01:29:39 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-856bb2f81dfb6dae1bc33b3c3d55b30c990037ccc6da70f3e10ae7f6c13cf841.tar.gz"  && echo "e1f981f4d077e2f832d9a9e5a8e34dd9f16ced8725a897d90b3dcf79799481f9  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a94ca19f706b0fae65365af76666c91188cb9f6b7a6548a162179b4e34124d53`  
		Last Modified: Tue, 22 Oct 2019 01:30:58 GMT  
		Size: 62.2 MB (62152740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75afe2eae0ca1c4eba3f912c5116c0967b8c4e64ed45e11778684cd9a0cf532`  
		Last Modified: Tue, 22 Oct 2019 01:31:23 GMT  
		Size: 324.9 MB (324927212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:58d05c596a29f2cfb81543dddd01ca5613bc33e2a65a5567dc875d50e7225f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:62f2d2d01cbe3b8932a7bb7edb3253444d743cf2123f3bc0c9821b275e431f4f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61552853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3850f151f1dbfebe4263a9b95ad8f5f43a1c8dc0b299d651813197be914c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:49ed0d5c99b7b00780d1f54e1cd311e606926421a7cbda54a05a29768880c819
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62796733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a4023fdbe1650d07218c2dca7a96d9b12488b7f01566c449a6ccfd53dceb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:5ded99e84532e28bbcf5ad466aeddc54eca2622a21e6f393cc6469c6ca8b1d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2e02adc1f2114a6efea2c06ba99c90ad3d5028d6c782c1210217204aa6f2aa9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62152740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1f3d6c1c4519a5ebb30495a78988409b2a8ffe4f06b1e620fa48b200f217d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 22 Oct 2019 01:29:16 GMT
ADD file:4a60739abc789db5501d860d9d7f1ccaa4b9a062c2f77adc7620d26b9331a4ad in / 
# Tue, 22 Oct 2019 01:29:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a94ca19f706b0fae65365af76666c91188cb9f6b7a6548a162179b4e34124d53`  
		Last Modified: Tue, 22 Oct 2019 01:30:58 GMT  
		Size: 62.2 MB (62152740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20191219.0`

**does not exist** (yet?)

## `amazonlinux:2018.03.0.20191219.0-with-sources`

**does not exist** (yet?)

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:292f57784050dc780d7ce9660795fa17204a03062c19d761ab958d28901ba63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e7562fd6a35798d6b003775bb0a2fb0c026e6433dd768d7fc3284bd900f603db
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387079952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4907fefc006913ec52f7d599f5b27afe493ac2a55e5b6ca1b8c9de838275929`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 22 Oct 2019 01:29:16 GMT
ADD file:4a60739abc789db5501d860d9d7f1ccaa4b9a062c2f77adc7620d26b9331a4ad in / 
# Tue, 22 Oct 2019 01:29:16 GMT
CMD ["/bin/bash"]
# Tue, 22 Oct 2019 01:29:39 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-856bb2f81dfb6dae1bc33b3c3d55b30c990037ccc6da70f3e10ae7f6c13cf841.tar.gz"  && echo "e1f981f4d077e2f832d9a9e5a8e34dd9f16ced8725a897d90b3dcf79799481f9  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a94ca19f706b0fae65365af76666c91188cb9f6b7a6548a162179b4e34124d53`  
		Last Modified: Tue, 22 Oct 2019 01:30:58 GMT  
		Size: 62.2 MB (62152740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75afe2eae0ca1c4eba3f912c5116c0967b8c4e64ed45e11778684cd9a0cf532`  
		Last Modified: Tue, 22 Oct 2019 01:31:23 GMT  
		Size: 324.9 MB (324927212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20191217.0`

```console
$ docker pull amazonlinux@sha256:58d05c596a29f2cfb81543dddd01ca5613bc33e2a65a5567dc875d50e7225f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20191217.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:62f2d2d01cbe3b8932a7bb7edb3253444d743cf2123f3bc0c9821b275e431f4f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61552853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3850f151f1dbfebe4263a9b95ad8f5f43a1c8dc0b299d651813197be914c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20191217.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:49ed0d5c99b7b00780d1f54e1cd311e606926421a7cbda54a05a29768880c819
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62796733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a4023fdbe1650d07218c2dca7a96d9b12488b7f01566c449a6ccfd53dceb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20191217.0-with-sources`

```console
$ docker pull amazonlinux@sha256:4c783009560a5f08a4d623c73eaeda37fe1ee471eadedd3367134b2312a1c253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20191217.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0d9f1e0225df93bd2bba70f617f89179a127521cad15e17a6dbcde76dbfdc843
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.6 MB (476630585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf287040157831d59644400a2ebe9282a4a2958806dd9aaec89f45a4b60676`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46f1f3757b9b441219f29d7c37d98f714a2d5d0043cc2a6b4151e4041bfb47c`  
		Last Modified: Fri, 10 Jan 2020 00:21:18 GMT  
		Size: 415.1 MB (415077732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20191217.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:333ab3c09fcd688afb8ff5c72ae49a75124e92f75a06905dba9f762aeaaf8de9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.9 MB (477874498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0c7fbcfbe94cabe2f0115ee5fc3f669abb53d528cf8dd34fe81e7a893f8f3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2020 23:46:21 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34e86703318f8a60930cd62ad26d01ef97a89085a74d36f8924c8584468424`  
		Last Modified: Thu, 09 Jan 2020 23:48:04 GMT  
		Size: 415.1 MB (415077765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:4c783009560a5f08a4d623c73eaeda37fe1ee471eadedd3367134b2312a1c253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0d9f1e0225df93bd2bba70f617f89179a127521cad15e17a6dbcde76dbfdc843
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.6 MB (476630585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf287040157831d59644400a2ebe9282a4a2958806dd9aaec89f45a4b60676`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46f1f3757b9b441219f29d7c37d98f714a2d5d0043cc2a6b4151e4041bfb47c`  
		Last Modified: Fri, 10 Jan 2020 00:21:18 GMT  
		Size: 415.1 MB (415077732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:333ab3c09fcd688afb8ff5c72ae49a75124e92f75a06905dba9f762aeaaf8de9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.9 MB (477874498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0c7fbcfbe94cabe2f0115ee5fc3f669abb53d528cf8dd34fe81e7a893f8f3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2020 23:46:21 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34e86703318f8a60930cd62ad26d01ef97a89085a74d36f8924c8584468424`  
		Last Modified: Thu, 09 Jan 2020 23:48:04 GMT  
		Size: 415.1 MB (415077765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:58d05c596a29f2cfb81543dddd01ca5613bc33e2a65a5567dc875d50e7225f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:62f2d2d01cbe3b8932a7bb7edb3253444d743cf2123f3bc0c9821b275e431f4f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61552853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3850f151f1dbfebe4263a9b95ad8f5f43a1c8dc0b299d651813197be914c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:49ed0d5c99b7b00780d1f54e1cd311e606926421a7cbda54a05a29768880c819
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62796733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a4023fdbe1650d07218c2dca7a96d9b12488b7f01566c449a6ccfd53dceb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:4c783009560a5f08a4d623c73eaeda37fe1ee471eadedd3367134b2312a1c253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0d9f1e0225df93bd2bba70f617f89179a127521cad15e17a6dbcde76dbfdc843
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.6 MB (476630585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf287040157831d59644400a2ebe9282a4a2958806dd9aaec89f45a4b60676`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46f1f3757b9b441219f29d7c37d98f714a2d5d0043cc2a6b4151e4041bfb47c`  
		Last Modified: Fri, 10 Jan 2020 00:21:18 GMT  
		Size: 415.1 MB (415077732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:333ab3c09fcd688afb8ff5c72ae49a75124e92f75a06905dba9f762aeaaf8de9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.9 MB (477874498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0c7fbcfbe94cabe2f0115ee5fc3f669abb53d528cf8dd34fe81e7a893f8f3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2020 23:46:21 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34e86703318f8a60930cd62ad26d01ef97a89085a74d36f8924c8584468424`  
		Last Modified: Thu, 09 Jan 2020 23:48:04 GMT  
		Size: 415.1 MB (415077765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
