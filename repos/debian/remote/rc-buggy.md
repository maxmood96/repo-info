## `debian:rc-buggy`

```console
$ docker pull debian@sha256:255cdf1da2ce7a63d1a304ab42b9140546f1ec0b8f882a511e13370f0cc8fe85
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
$ docker pull debian@sha256:adf0d2bd9dd78f04a9302039c67b8f6cd24902c76bdf165479b5a87339f8522b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49299495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dd3ddbf1b5d9f253804360c2b3867fef28ba734ec2e4c1fd58000dd02ad9b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:42 GMT
ADD file:6261ecb921e04d2b3f6fd44e5dcb5683154bc0beee4f26913c2be9395a060489 in / 
# Tue, 02 May 2023 23:47:43 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:48:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ae396e350f30e1defad1bfa67a84b97389d42cf3442551e39a0e2bab6b53a50c`  
		Last Modified: Tue, 02 May 2023 23:51:56 GMT  
		Size: 49.3 MB (49299270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab32f0e5b01921ccdf97f71444ebd25998f7c2cdbdc6d473421801454fd949b`  
		Last Modified: Tue, 02 May 2023 23:53:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:483154564a48970e5c12a396e1746485bfb6bc245df4982fc7071d460290058a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ececf4ea3db752a8bf79e9ec60707ad2250bdf5eae117483fd02e6c3acc2daf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:49 GMT
ADD file:bbdd13db0e090d7d928a2beba57e3c1340342d05e5c15f7b7377c9791a5cb4ba in / 
# Tue, 23 May 2023 00:48:50 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:49:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d14a321d144fc48aa438b2364b0f1a5667979322ef9cada9309bca48584a11a1`  
		Last Modified: Tue, 23 May 2023 00:51:36 GMT  
		Size: 47.2 MB (47154613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e3404f665334f67249172ac844a47f1e79bb25e3d0cb849f3671a54ff10585`  
		Last Modified: Tue, 23 May 2023 00:53:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:c14446c1867b4a1aed7c99003206cdad719bb142f7d27e0c8eaa5fac389c1b75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44981526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4981c49750a38199f8f6129b83a4086acf0307ff9e3c93c5e47571966b1b6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:58:50 GMT
ADD file:d575865c0ae8f8ca887a39f651f9e4f5ec16e2f0233bba91239c33ac167a8bf0 in / 
# Tue, 23 May 2023 00:58:51 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:00:09 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d28602ae46d2f07ea10d44c6edf1cf2be8bec1552141a793411caab17bdf1d13`  
		Last Modified: Tue, 23 May 2023 01:03:14 GMT  
		Size: 45.0 MB (44981303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ecad73e9cbd417508b5e8e109281e08c219d29cb5395fb2cad347b813f7487`  
		Last Modified: Tue, 23 May 2023 01:05:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:948ecfefda3ca8e1c8af2f2ae638e4a41e1a73612852d3ddba20551c6bf50cbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49336524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc227954a86f424939bd1883fe8b6f4ee2649b861844569c7e2c9f34d41ab881`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:48 GMT
ADD file:4608b82b211b6814e5bf372be706a6c01bd7a2a4841b59ac5430ec3a3f94468d in / 
# Tue, 23 May 2023 00:43:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:36 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5842d200e3f7df637a96b64f14e82ccb2c66e201137165f2d91447fbd3248a8c`  
		Last Modified: Tue, 23 May 2023 00:47:31 GMT  
		Size: 49.3 MB (49336298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d16b96418f665018572e36c1d3858326b529c4059b207df0620f14f598584`  
		Last Modified: Tue, 23 May 2023 00:49:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:8b7c6323d66c79f3b436846e7580f1866bf5470fdaa46df6a3a4b7f259fe62c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50311722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d52f52a0f46e1c4c785e7e7baa2c614c36bd70386aaf7303108acad34ed1801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:40:47 GMT
ADD file:33dd3eb2725f92170606ce015e99cc9496d244630b3f4844cb8f3f61b16e2eb0 in / 
# Tue, 23 May 2023 00:40:48 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:42:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1034171b4bde64cf8e4ff854704a3bf68000eddcceb63b481197082dced785ba`  
		Last Modified: Tue, 23 May 2023 00:46:09 GMT  
		Size: 50.3 MB (50311497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef221bf7ed0e5804a93644fffecc4abab1053075bfb0deee1cc55923e052e44d`  
		Last Modified: Tue, 23 May 2023 00:48:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:b2dc774956b49f2d795ebf4a5d2f48f11595faf2eaccc4cbc3b8ad733c9745f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b8aca8a670e244c1d0a36ee73ee85acecd4532ebfa8429bf55271585299b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:50:24 GMT
ADD file:3eff171361a4eb801d0fe38f81ca109a46285fd25a23f84aa338364d49c0591d in / 
# Tue, 02 May 2023 23:50:30 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:55:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6ad09064fad2597f74f486eca3ca74c1f51072bf61093439cd70c0d5735689aa`  
		Last Modified: Tue, 02 May 2023 23:58:51 GMT  
		Size: 49.3 MB (49301428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4847ad1197d2126466856d709175b88386daf4ca58f1635df5bfd689d7bb2030`  
		Last Modified: Wed, 03 May 2023 00:03:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:39f24d94e5ca8acf6e96c44ac9a28065a5a760e756a6fdc397c97f6696072e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53307461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c770209c7bcee8625097cdb81b3c03a858198ffe23d831c48e56d8b62cf2f430`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:32:10 GMT
ADD file:c9bb656a5f751ff13849f6ca569f657cfc8dbe757b270dfa6e9fe2181e699494 in / 
# Wed, 03 May 2023 00:32:13 GMT
CMD ["bash"]
# Wed, 03 May 2023 00:34:54 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:71d18ac463268aeb15f1776de10a379de577489dfb1022fc92adf6187695aeeb`  
		Last Modified: Wed, 03 May 2023 00:37:22 GMT  
		Size: 53.3 MB (53307234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd66c0990deb8bcc0d2aa74ec53f7467ccd14ae84e3fa2b8e817eda07f2ea13`  
		Last Modified: Wed, 03 May 2023 00:40:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:84e35182aabe24cb59a5664c253dcdaf2dfc5a34ec3abcc5b5318eed2f841ee5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47664842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ef5ea7483c30d687bee61eb1a2e0fd884462bdb7e86c9dfe6b118a849d3b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:02 GMT
ADD file:7a71212c59dd3640d3ec2c6d4fd4df4a864f77e634571c1e200a6f7877a02cb2 in / 
# Tue, 23 May 2023 00:43:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:021a3707435b37ce556f1886fb9417a47cbfa836555f680d70cffb85f96a6eec`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 47.7 MB (47664615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf18678c08e741e18d3e68d1e057a69c98ac089b51c0c6cec761803ddb321f`  
		Last Modified: Tue, 23 May 2023 00:47:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
