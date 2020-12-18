<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03.0.20201028.0`](#amazonlinux2018030202010280)
-	[`amazonlinux:2018.03.0.20201028.0-with-sources`](#amazonlinux2018030202010280-with-sources)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2.0.20201111.0`](#amazonlinux20202011110)
-	[`amazonlinux:2.0.20201111.0-with-sources`](#amazonlinux20202011110-with-sources)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:b13cdf0453417bd9244f108f3d64eb8cd3a824b0049756ba94a7d959b7712f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:341f6e586fa0a42507d91d7f27936649f03fe674e0f4eca6b6b852c5ad6729c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62373863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c28984a7bca8f1fba2491ceac406006e0c134d8fdc1cbfec032018cd9b858f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:05:16 GMT
ADD file:2683b3f0ac78164c1c20573c3d932ca68bc64a2476a6425dbea13cd5f034e45a in / 
# Fri, 18 Dec 2020 07:05:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bff4388f7b75ad1360b990f47d0eb351256093e330c129e8eaf8dc77415c0643`  
		Last Modified: Fri, 18 Dec 2020 07:06:57 GMT  
		Size: 62.4 MB (62373863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:2579aa05851baa43ccb54ba2a367650bddcfac476d8a4a80403b864d193233a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f06ab271a91ce339a3e47de34f9a38ad8301b72db0c92f773341dcc8c0713477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449233684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534630d570deab085a09f4fc1f661eeb330cdbb8e14be87a2461c39316c867f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:05:16 GMT
ADD file:2683b3f0ac78164c1c20573c3d932ca68bc64a2476a6425dbea13cd5f034e45a in / 
# Fri, 18 Dec 2020 07:05:17 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:40 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c9551a4497cae21155e1d2f190af3804f239e04838f09b1f1558b342bfe09e09.tar.gz"  && echo "7ff2f8fe6b47e805c892b96118395dc7e4030f600f345f78a85a8c614fb0cfaf  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:bff4388f7b75ad1360b990f47d0eb351256093e330c129e8eaf8dc77415c0643`  
		Last Modified: Fri, 18 Dec 2020 07:06:57 GMT  
		Size: 62.4 MB (62373863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c036ff5ebaac47f265039b1e8a5b01b8f5bb2658a8de3dcb8125fbc5ccead71`  
		Last Modified: Fri, 18 Dec 2020 07:07:21 GMT  
		Size: 386.9 MB (386859821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:e87ffde799fd6e9c70c6ffb190726c146aeb1ae4d7667848850d9a609e7a7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2a83705487ebf18d7d3a2b1fc5eba8509676fa97384c568f6139bbbd8e5124b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b176d96bdc945bb6db21b54d7dc2cf907d412656834e0bf4b112c00c313251b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:45432827a9886949d2a5a97ad4fce1c69bc6078d0627b67e893c71b7f758aad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c58753c370914824f30cba19b77f0e3da15d77a636c8cacdb202d23614fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:b13cdf0453417bd9244f108f3d64eb8cd3a824b0049756ba94a7d959b7712f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:341f6e586fa0a42507d91d7f27936649f03fe674e0f4eca6b6b852c5ad6729c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62373863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c28984a7bca8f1fba2491ceac406006e0c134d8fdc1cbfec032018cd9b858f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:05:16 GMT
ADD file:2683b3f0ac78164c1c20573c3d932ca68bc64a2476a6425dbea13cd5f034e45a in / 
# Fri, 18 Dec 2020 07:05:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bff4388f7b75ad1360b990f47d0eb351256093e330c129e8eaf8dc77415c0643`  
		Last Modified: Fri, 18 Dec 2020 07:06:57 GMT  
		Size: 62.4 MB (62373863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20201028.0`

```console
$ docker pull amazonlinux@sha256:b13cdf0453417bd9244f108f3d64eb8cd3a824b0049756ba94a7d959b7712f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20201028.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:341f6e586fa0a42507d91d7f27936649f03fe674e0f4eca6b6b852c5ad6729c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62373863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c28984a7bca8f1fba2491ceac406006e0c134d8fdc1cbfec032018cd9b858f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:05:16 GMT
ADD file:2683b3f0ac78164c1c20573c3d932ca68bc64a2476a6425dbea13cd5f034e45a in / 
# Fri, 18 Dec 2020 07:05:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bff4388f7b75ad1360b990f47d0eb351256093e330c129e8eaf8dc77415c0643`  
		Last Modified: Fri, 18 Dec 2020 07:06:57 GMT  
		Size: 62.4 MB (62373863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20201028.0-with-sources`

```console
$ docker pull amazonlinux@sha256:2579aa05851baa43ccb54ba2a367650bddcfac476d8a4a80403b864d193233a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20201028.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f06ab271a91ce339a3e47de34f9a38ad8301b72db0c92f773341dcc8c0713477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449233684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534630d570deab085a09f4fc1f661eeb330cdbb8e14be87a2461c39316c867f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:05:16 GMT
ADD file:2683b3f0ac78164c1c20573c3d932ca68bc64a2476a6425dbea13cd5f034e45a in / 
# Fri, 18 Dec 2020 07:05:17 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:40 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c9551a4497cae21155e1d2f190af3804f239e04838f09b1f1558b342bfe09e09.tar.gz"  && echo "7ff2f8fe6b47e805c892b96118395dc7e4030f600f345f78a85a8c614fb0cfaf  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:bff4388f7b75ad1360b990f47d0eb351256093e330c129e8eaf8dc77415c0643`  
		Last Modified: Fri, 18 Dec 2020 07:06:57 GMT  
		Size: 62.4 MB (62373863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c036ff5ebaac47f265039b1e8a5b01b8f5bb2658a8de3dcb8125fbc5ccead71`  
		Last Modified: Fri, 18 Dec 2020 07:07:21 GMT  
		Size: 386.9 MB (386859821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:2579aa05851baa43ccb54ba2a367650bddcfac476d8a4a80403b864d193233a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f06ab271a91ce339a3e47de34f9a38ad8301b72db0c92f773341dcc8c0713477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449233684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534630d570deab085a09f4fc1f661eeb330cdbb8e14be87a2461c39316c867f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:05:16 GMT
ADD file:2683b3f0ac78164c1c20573c3d932ca68bc64a2476a6425dbea13cd5f034e45a in / 
# Fri, 18 Dec 2020 07:05:17 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:40 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c9551a4497cae21155e1d2f190af3804f239e04838f09b1f1558b342bfe09e09.tar.gz"  && echo "7ff2f8fe6b47e805c892b96118395dc7e4030f600f345f78a85a8c614fb0cfaf  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:bff4388f7b75ad1360b990f47d0eb351256093e330c129e8eaf8dc77415c0643`  
		Last Modified: Fri, 18 Dec 2020 07:06:57 GMT  
		Size: 62.4 MB (62373863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c036ff5ebaac47f265039b1e8a5b01b8f5bb2658a8de3dcb8125fbc5ccead71`  
		Last Modified: Fri, 18 Dec 2020 07:07:21 GMT  
		Size: 386.9 MB (386859821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20201111.0`

```console
$ docker pull amazonlinux@sha256:e87ffde799fd6e9c70c6ffb190726c146aeb1ae4d7667848850d9a609e7a7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20201111.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2a83705487ebf18d7d3a2b1fc5eba8509676fa97384c568f6139bbbd8e5124b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b176d96bdc945bb6db21b54d7dc2cf907d412656834e0bf4b112c00c313251b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20201111.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:45432827a9886949d2a5a97ad4fce1c69bc6078d0627b67e893c71b7f758aad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c58753c370914824f30cba19b77f0e3da15d77a636c8cacdb202d23614fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20201111.0-with-sources`

```console
$ docker pull amazonlinux@sha256:5ac935a5c036738010379d35b4de557da6b237b48be3662f56ed4dd0c56c5d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20201111.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6380e690beefb9299002207588d8355ced97807753d21577df24ebb493dcf247
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542819174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2b0c7efa71a10e9a135b04bc5f5f7c1fd4d52486d4fee73ec42db1b7b7db72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:02 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c9c4dcbe7d80a1586ec7d143bf92d28c1644fbc92b3be20b0d99e271b4c44b`  
		Last Modified: Fri, 18 Dec 2020 07:06:38 GMT  
		Size: 480.8 MB (480810655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20201111.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:5ac935a5c036738010379d35b4de557da6b237b48be3662f56ed4dd0c56c5d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6380e690beefb9299002207588d8355ced97807753d21577df24ebb493dcf247
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542819174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2b0c7efa71a10e9a135b04bc5f5f7c1fd4d52486d4fee73ec42db1b7b7db72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:02 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c9c4dcbe7d80a1586ec7d143bf92d28c1644fbc92b3be20b0d99e271b4c44b`  
		Last Modified: Fri, 18 Dec 2020 07:06:38 GMT  
		Size: 480.8 MB (480810655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:e87ffde799fd6e9c70c6ffb190726c146aeb1ae4d7667848850d9a609e7a7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2a83705487ebf18d7d3a2b1fc5eba8509676fa97384c568f6139bbbd8e5124b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b176d96bdc945bb6db21b54d7dc2cf907d412656834e0bf4b112c00c313251b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:45432827a9886949d2a5a97ad4fce1c69bc6078d0627b67e893c71b7f758aad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c58753c370914824f30cba19b77f0e3da15d77a636c8cacdb202d23614fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:5ac935a5c036738010379d35b4de557da6b237b48be3662f56ed4dd0c56c5d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6380e690beefb9299002207588d8355ced97807753d21577df24ebb493dcf247
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542819174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2b0c7efa71a10e9a135b04bc5f5f7c1fd4d52486d4fee73ec42db1b7b7db72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:02 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c9c4dcbe7d80a1586ec7d143bf92d28c1644fbc92b3be20b0d99e271b4c44b`  
		Last Modified: Fri, 18 Dec 2020 07:06:38 GMT  
		Size: 480.8 MB (480810655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
