## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:3f397d2321c26abfb373c1f4ca601902d6c0d7ff763cf9c315bad79cf2c529b0
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:480aa48e405021523db6cef1756c65127d004bf70cc973bc13be30253eaa7cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52944624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1d7e3175ecd8da60fec8a2f9deeb250e8677aaafd4f5b7d0dc16a6a315c941`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:19:44 GMT
ADD file:daaac4875b34dee73ff062c17a4763b2cf5726753df4e9700bbcefa0f88153e6 in / 
# Wed, 11 May 2022 01:19:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:19:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d68396ae84f0ca729923a79943893f43492725d77e7b329170777a2bdbb6752b`  
		Last Modified: Wed, 11 May 2022 01:24:08 GMT  
		Size: 52.9 MB (52944400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4aace0849c4b5772ca1b127ee42e7ce2b815d1883e45091c0c29ce801704e8`  
		Last Modified: Wed, 11 May 2022 01:24:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a8501c9515935127315dd8c83a61d3b162f88c0150aceeead01d3fff6b6c87ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50737662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ac339cb6aaa786b3a5446a53bc3576375780a2988e5e783b9e73f84dd6890a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:49:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd980aa5c298f4abd497f7d74bcbfaaa37a9105bd53353acd861dfeeac5218e`  
		Last Modified: Wed, 11 May 2022 01:03:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1e40ae6bfb74600d6a6f94bfed9a67bd01566e38454357673d53ccff05db32bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48476143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bd98103795bd4d0bf4490bda3c41aa6eebde15898d2328fe3c317c3ac43e76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:47:29 GMT
ADD file:ae0b1a579333a3c7912430243fe91f71f32d0e234d52667dd937f7cd23a8d3d2 in / 
# Wed, 11 May 2022 01:47:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:47:42 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1fdc9e441250146f7b7c78b0264138dc69a0b46d264373157ac1c2cdba7a552d`  
		Last Modified: Wed, 11 May 2022 02:02:37 GMT  
		Size: 48.5 MB (48475916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6d62e4957d4bcd081c037ee826e9a4f2e774ada017c8a590182604cde6854`  
		Last Modified: Wed, 11 May 2022 02:02:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:56c139c5dbda4ffb4c0a3807b5585598bcf25b1eb1d536da0c0ae2bdd70a86fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52041568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a008465d47f0b9f31f31c4a2c58727757c0a8a0dfed9561583cfa766bf19d36f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:19 GMT
ADD file:a50b6ecf9ed84e6e3bb43f96fd036c7ebaad7f94df16c3637d6dd19a6dc91701 in / 
# Wed, 11 May 2022 00:46:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:46:27 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45306f5029ed7ce5685e65dccfaecf3f4a79040520f3ffb65eac76781218fea1`  
		Last Modified: Wed, 11 May 2022 00:52:36 GMT  
		Size: 52.0 MB (52041343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962fa68fe5d569c465d574454e5db20145977bb9d3ede454d5142e277a89fcda`  
		Last Modified: Wed, 11 May 2022 00:52:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:346fba994202ae0bd0ffab243694866d7e642efeab0b50aafa6aa27dc926e5ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53944970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0762731ce31f3ab7122fca89da8ec91119b70c9858688fa14361579a300dfb9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:38:30 GMT
ADD file:ba0a6f659c101ad7b3c77be40e790f4ec4576f59a39c794974d82b28b115788d in / 
# Wed, 11 May 2022 01:38:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:38:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca5b88a4b2f0398218cdfea0aee4d6b7cd7ae535feeb27719eb9603a02ef7752`  
		Last Modified: Wed, 11 May 2022 01:45:11 GMT  
		Size: 53.9 MB (53944746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8334d65a0f8ad18caa1506840b1de4538f4f51764fb74bb16662012272bd02`  
		Last Modified: Wed, 11 May 2022 01:45:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7228f0792c34a92098cd9bb4941b2e2a7f9d80ee761c77dfabcb9ec915d11439
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52067153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94fefdd36cb9d01a7c65e784de2ed6091d3068d91082353258a5d7c93576419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:21:42 GMT
ADD file:023ba5f785e781bda7875c3b4c2f163666fe7b1a6a0fde74103b7799380a55c3 in / 
# Wed, 11 May 2022 02:21:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:22:04 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1315838dc3fae911b53ad8b9fdb88cdc4a2988e4a4924922837b71b52b18d1fa`  
		Last Modified: Wed, 11 May 2022 02:31:44 GMT  
		Size: 52.1 MB (52066926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331a3fd2008c235f27643acab53e658bc853c66379aa40daf350af5b007de45e`  
		Last Modified: Wed, 11 May 2022 02:31:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:90cd0206a700ff29019715348fe34353bba280cb3a2ba8a783bcd743f189c1f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57150668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45203d37759f674b0535fd654e695f019b61893d540496238a282a154a94310c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:31:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c7c04802d3e0303cdf2e095017f859003c5895804d9ca1ed1d5164bdfbe65`  
		Last Modified: Wed, 11 May 2022 01:41:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:04c430b35b9a86898fe020228a914b0b4d92a9cff28e836da84b9631ce78b859
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51484197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a234faa76ab35a4e6d70202f2e267cebe619a053d0f05ecff8eab7b17bb9d604`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:43:27 GMT
ADD file:d38e77e014746a6349342f7d1cb5eada86f6e06423bf095efa6f182b4d038b77 in / 
# Wed, 11 May 2022 00:43:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:43:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b3467d807091357239fe13d54d3572c25afe85ac06c182eba9268af6bac8f48a`  
		Last Modified: Wed, 11 May 2022 00:49:13 GMT  
		Size: 51.5 MB (51483972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7931922ab0a41c42a8c4d77438d0eb3c3a444db19f95ba63cdb79af9f4245c86`  
		Last Modified: Wed, 11 May 2022 00:49:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
