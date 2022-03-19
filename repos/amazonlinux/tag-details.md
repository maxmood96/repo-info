<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20220316.0`](#amazonlinux20202203160)
-	[`amazonlinux:2.0.20220316.0-with-sources`](#amazonlinux20202203160-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20220315.0`](#amazonlinux2018030202203150)
-	[`amazonlinux:2018.03.0.20220315.0-with-sources`](#amazonlinux2018030202203150-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20220308.1`](#amazonlinux20220202203081)
-	[`amazonlinux:2022.0.20220308.1-with-sources`](#amazonlinux20220202203081-with-sources)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:devel-with-sources`](#amazonlinuxdevel-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:6d6d23596b807105d3aa54ceda05fef7f08ab8bcd48cd6bec6f216111c2e26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6b88dfac47108b50d5f76fe09cfcbcc16c06e1ea8b97c60ff4041f8a3da00282
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62371377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b51c1998f54dfd2111136ee5fb8c322fed50b421aed9c334a3d47028757503`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 00:00:30 GMT
ADD file:0740e257922976a4807eb5e0e8b2137d2187c581e04757bc6396b012c2984877 in / 
# Sat, 19 Mar 2022 00:00:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a2af4276da118f47f6d59faaf739ac8ad6b76230fe4e9e881f931f89f5fe99d`  
		Last Modified: Sat, 19 Mar 2022 00:01:39 GMT  
		Size: 62.4 MB (62371377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:cab807063eba14c13141f4ca54c68b85b13466402ac0aa3b103fddd9aa71b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:61dd738d5d2d0e86bf529be79608e492643297824b2528559b9356b76699b013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515016086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c0893271a92f18800485ea04292041280f69c87a1a4c15d98fba808bd1ed14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 00:00:30 GMT
ADD file:0740e257922976a4807eb5e0e8b2137d2187c581e04757bc6396b012c2984877 in / 
# Sat, 19 Mar 2022 00:00:31 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:00:56 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-1955409f03009ae852836cca134addda0273353334d33438c74060317a23bd38.tar.gz"  && echo "3d9d1fa76eb7d2d554881174fd0f92549d482d99b6f60822dd59173789b14ddc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6a2af4276da118f47f6d59faaf739ac8ad6b76230fe4e9e881f931f89f5fe99d`  
		Last Modified: Sat, 19 Mar 2022 00:01:39 GMT  
		Size: 62.4 MB (62371377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298f23d3684e32a3c17a32933ec4af8f46adeddc4abcf14615c8bb052dedf445`  
		Last Modified: Sat, 19 Mar 2022 00:02:14 GMT  
		Size: 452.6 MB (452644709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:b33b787cdb0e82495d2dc115745f68c7cd8d2585d9d83812fdc183ad39d1b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6fa3c5cd2dc7efbe15a2f1d888e8791819023b0d21ae4de3f8014b6b7cf2be10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62205270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa63ff55c40363d84978d0bd4f41d56d7d4bf4b33a7ea1f30d94b6a0dce6323`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f3585a47bc028e750f37684bbf67de38d2c5ae102b8742405c4fa2364647863a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63828887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048c8ea90cafeac8f911ba460a0a6924d8d056a9caf220a8628458a5f6ba77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:21693ea27108e5514cd3fce013a53ea08b32e2ad6dd9d3263f38bf9c3bab6e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:482a94c2fbb091d98d5f458dad127758f4774d6c850386b8e9f637099fa92463
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.3 MB (485327027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4553ac9cb419bbc8bf2268c081472d5ef9ae180c2f978ef628deed7ca6fa414`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:26:52 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-3c9668ec048dfa6db814960c8f21d657525398c311820322e74a0cd5c740a565.tar.gz"  && echo "28f895ddb81eab8d861e7f1adc7c54a47146dc14956644e699d4eb9ead29f515  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49cb7dc0d9e4a04a4e0043db8324496b140ebf112a0615b6975552ed5e9f9a`  
		Last Modified: Fri, 18 Mar 2022 05:28:47 GMT  
		Size: 423.1 MB (423121757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:eb66bea13e8eb8b6402f2396470190f5201029f1740f7571511d66fdd157dcdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2615f7bdf3f4ddc681610c299da2d5c5c1dfb862ccb4e2f3c5ff0558c98ff73f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:23 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-3c9668ec048dfa6db814960c8f21d657525398c311820322e74a0cd5c740a565.tar.gz"  && echo "28f895ddb81eab8d861e7f1adc7c54a47146dc14956644e699d4eb9ead29f515  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cd7a9d9c15edb2f1e103b9fc3acb6251a5ee9d252dae649c8d9c61b88973b5`  
		Last Modified: Fri, 18 Mar 2022 00:39:16 GMT  
		Size: 423.1 MB (423121720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220316.0`

```console
$ docker pull amazonlinux@sha256:b33b787cdb0e82495d2dc115745f68c7cd8d2585d9d83812fdc183ad39d1b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220316.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6fa3c5cd2dc7efbe15a2f1d888e8791819023b0d21ae4de3f8014b6b7cf2be10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62205270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa63ff55c40363d84978d0bd4f41d56d7d4bf4b33a7ea1f30d94b6a0dce6323`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220316.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f3585a47bc028e750f37684bbf67de38d2c5ae102b8742405c4fa2364647863a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63828887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048c8ea90cafeac8f911ba460a0a6924d8d056a9caf220a8628458a5f6ba77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220316.0-with-sources`

```console
$ docker pull amazonlinux@sha256:21693ea27108e5514cd3fce013a53ea08b32e2ad6dd9d3263f38bf9c3bab6e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220316.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:482a94c2fbb091d98d5f458dad127758f4774d6c850386b8e9f637099fa92463
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.3 MB (485327027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4553ac9cb419bbc8bf2268c081472d5ef9ae180c2f978ef628deed7ca6fa414`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:26:52 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-3c9668ec048dfa6db814960c8f21d657525398c311820322e74a0cd5c740a565.tar.gz"  && echo "28f895ddb81eab8d861e7f1adc7c54a47146dc14956644e699d4eb9ead29f515  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49cb7dc0d9e4a04a4e0043db8324496b140ebf112a0615b6975552ed5e9f9a`  
		Last Modified: Fri, 18 Mar 2022 05:28:47 GMT  
		Size: 423.1 MB (423121757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220316.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:eb66bea13e8eb8b6402f2396470190f5201029f1740f7571511d66fdd157dcdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2615f7bdf3f4ddc681610c299da2d5c5c1dfb862ccb4e2f3c5ff0558c98ff73f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:23 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-3c9668ec048dfa6db814960c8f21d657525398c311820322e74a0cd5c740a565.tar.gz"  && echo "28f895ddb81eab8d861e7f1adc7c54a47146dc14956644e699d4eb9ead29f515  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cd7a9d9c15edb2f1e103b9fc3acb6251a5ee9d252dae649c8d9c61b88973b5`  
		Last Modified: Fri, 18 Mar 2022 00:39:16 GMT  
		Size: 423.1 MB (423121720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:6d6d23596b807105d3aa54ceda05fef7f08ab8bcd48cd6bec6f216111c2e26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6b88dfac47108b50d5f76fe09cfcbcc16c06e1ea8b97c60ff4041f8a3da00282
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62371377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b51c1998f54dfd2111136ee5fb8c322fed50b421aed9c334a3d47028757503`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 00:00:30 GMT
ADD file:0740e257922976a4807eb5e0e8b2137d2187c581e04757bc6396b012c2984877 in / 
# Sat, 19 Mar 2022 00:00:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a2af4276da118f47f6d59faaf739ac8ad6b76230fe4e9e881f931f89f5fe99d`  
		Last Modified: Sat, 19 Mar 2022 00:01:39 GMT  
		Size: 62.4 MB (62371377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:cab807063eba14c13141f4ca54c68b85b13466402ac0aa3b103fddd9aa71b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:61dd738d5d2d0e86bf529be79608e492643297824b2528559b9356b76699b013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515016086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c0893271a92f18800485ea04292041280f69c87a1a4c15d98fba808bd1ed14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 00:00:30 GMT
ADD file:0740e257922976a4807eb5e0e8b2137d2187c581e04757bc6396b012c2984877 in / 
# Sat, 19 Mar 2022 00:00:31 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:00:56 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-1955409f03009ae852836cca134addda0273353334d33438c74060317a23bd38.tar.gz"  && echo "3d9d1fa76eb7d2d554881174fd0f92549d482d99b6f60822dd59173789b14ddc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6a2af4276da118f47f6d59faaf739ac8ad6b76230fe4e9e881f931f89f5fe99d`  
		Last Modified: Sat, 19 Mar 2022 00:01:39 GMT  
		Size: 62.4 MB (62371377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298f23d3684e32a3c17a32933ec4af8f46adeddc4abcf14615c8bb052dedf445`  
		Last Modified: Sat, 19 Mar 2022 00:02:14 GMT  
		Size: 452.6 MB (452644709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220315.0`

```console
$ docker pull amazonlinux@sha256:6d6d23596b807105d3aa54ceda05fef7f08ab8bcd48cd6bec6f216111c2e26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220315.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6b88dfac47108b50d5f76fe09cfcbcc16c06e1ea8b97c60ff4041f8a3da00282
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62371377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b51c1998f54dfd2111136ee5fb8c322fed50b421aed9c334a3d47028757503`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 00:00:30 GMT
ADD file:0740e257922976a4807eb5e0e8b2137d2187c581e04757bc6396b012c2984877 in / 
# Sat, 19 Mar 2022 00:00:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a2af4276da118f47f6d59faaf739ac8ad6b76230fe4e9e881f931f89f5fe99d`  
		Last Modified: Sat, 19 Mar 2022 00:01:39 GMT  
		Size: 62.4 MB (62371377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220315.0-with-sources`

```console
$ docker pull amazonlinux@sha256:cab807063eba14c13141f4ca54c68b85b13466402ac0aa3b103fddd9aa71b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220315.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:61dd738d5d2d0e86bf529be79608e492643297824b2528559b9356b76699b013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515016086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c0893271a92f18800485ea04292041280f69c87a1a4c15d98fba808bd1ed14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 00:00:30 GMT
ADD file:0740e257922976a4807eb5e0e8b2137d2187c581e04757bc6396b012c2984877 in / 
# Sat, 19 Mar 2022 00:00:31 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:00:56 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-1955409f03009ae852836cca134addda0273353334d33438c74060317a23bd38.tar.gz"  && echo "3d9d1fa76eb7d2d554881174fd0f92549d482d99b6f60822dd59173789b14ddc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6a2af4276da118f47f6d59faaf739ac8ad6b76230fe4e9e881f931f89f5fe99d`  
		Last Modified: Sat, 19 Mar 2022 00:01:39 GMT  
		Size: 62.4 MB (62371377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298f23d3684e32a3c17a32933ec4af8f46adeddc4abcf14615c8bb052dedf445`  
		Last Modified: Sat, 19 Mar 2022 00:02:14 GMT  
		Size: 452.6 MB (452644709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022`

```console
$ docker pull amazonlinux@sha256:a78a435f32ae4290ac54a96f8cc56e682442a87aa18c3dc23f060f0cc3f29f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:51df946a4e4baa0703529bd96b0e4121707c15b95495e2a272a855bac49b5dbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67426158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7342cf9474f0fcaaf6ddfa98bf10892bd6730f0b3601d3af3688121c6883d3b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:72f24f745e7d92730a1d833c0e2d62a5cf2b34de0c28751361185695a94958b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66181332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05e07b335cebb522b1bf5d9bc24b6f3c7ce7058ee0d7e24db511662441d01e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:62789f043b2224eb1a3a2d3fedf8b67c36c0631869527698bb253a364b818b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:cec8782e7aaa5455f3a276dadc2e4297b28a62d6ecdb21cc0afc713434074829
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.9 MB (474946109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823312af76af409bdda4e70151d51c4713c210d1dba1b23c9521aa73bf1c35e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:27:34 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72f01cba51a2f374f99aaddd4380ba43b81e13d58c8ea7d85bb58c017ecfdb`  
		Last Modified: Fri, 18 Mar 2022 05:29:56 GMT  
		Size: 407.5 MB (407519951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:efa82a440427284fb42c3bb04f8b6883d1d25256b94825dedc674a5dbd4bf666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473701235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f7a9f1488c64f9e231d75c17a96d6c7861535370a772aa719bf6f9d439a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:58 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72833236772f911f636d1b918822c9a8ebd9cd41307464819b9beb9a35f16870`  
		Last Modified: Fri, 18 Mar 2022 00:40:21 GMT  
		Size: 407.5 MB (407519903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220308.1`

```console
$ docker pull amazonlinux@sha256:a78a435f32ae4290ac54a96f8cc56e682442a87aa18c3dc23f060f0cc3f29f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220308.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:51df946a4e4baa0703529bd96b0e4121707c15b95495e2a272a855bac49b5dbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67426158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7342cf9474f0fcaaf6ddfa98bf10892bd6730f0b3601d3af3688121c6883d3b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220308.1` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:72f24f745e7d92730a1d833c0e2d62a5cf2b34de0c28751361185695a94958b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66181332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05e07b335cebb522b1bf5d9bc24b6f3c7ce7058ee0d7e24db511662441d01e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220308.1-with-sources`

```console
$ docker pull amazonlinux@sha256:62789f043b2224eb1a3a2d3fedf8b67c36c0631869527698bb253a364b818b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220308.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:cec8782e7aaa5455f3a276dadc2e4297b28a62d6ecdb21cc0afc713434074829
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.9 MB (474946109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823312af76af409bdda4e70151d51c4713c210d1dba1b23c9521aa73bf1c35e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:27:34 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72f01cba51a2f374f99aaddd4380ba43b81e13d58c8ea7d85bb58c017ecfdb`  
		Last Modified: Fri, 18 Mar 2022 05:29:56 GMT  
		Size: 407.5 MB (407519951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220308.1-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:efa82a440427284fb42c3bb04f8b6883d1d25256b94825dedc674a5dbd4bf666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473701235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f7a9f1488c64f9e231d75c17a96d6c7861535370a772aa719bf6f9d439a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:58 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72833236772f911f636d1b918822c9a8ebd9cd41307464819b9beb9a35f16870`  
		Last Modified: Fri, 18 Mar 2022 00:40:21 GMT  
		Size: 407.5 MB (407519903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:a78a435f32ae4290ac54a96f8cc56e682442a87aa18c3dc23f060f0cc3f29f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:51df946a4e4baa0703529bd96b0e4121707c15b95495e2a272a855bac49b5dbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67426158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7342cf9474f0fcaaf6ddfa98bf10892bd6730f0b3601d3af3688121c6883d3b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:72f24f745e7d92730a1d833c0e2d62a5cf2b34de0c28751361185695a94958b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66181332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05e07b335cebb522b1bf5d9bc24b6f3c7ce7058ee0d7e24db511662441d01e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:62789f043b2224eb1a3a2d3fedf8b67c36c0631869527698bb253a364b818b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:cec8782e7aaa5455f3a276dadc2e4297b28a62d6ecdb21cc0afc713434074829
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.9 MB (474946109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823312af76af409bdda4e70151d51c4713c210d1dba1b23c9521aa73bf1c35e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:27:34 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72f01cba51a2f374f99aaddd4380ba43b81e13d58c8ea7d85bb58c017ecfdb`  
		Last Modified: Fri, 18 Mar 2022 05:29:56 GMT  
		Size: 407.5 MB (407519951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:efa82a440427284fb42c3bb04f8b6883d1d25256b94825dedc674a5dbd4bf666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473701235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f7a9f1488c64f9e231d75c17a96d6c7861535370a772aa719bf6f9d439a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:58 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72833236772f911f636d1b918822c9a8ebd9cd41307464819b9beb9a35f16870`  
		Last Modified: Fri, 18 Mar 2022 00:40:21 GMT  
		Size: 407.5 MB (407519903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:b33b787cdb0e82495d2dc115745f68c7cd8d2585d9d83812fdc183ad39d1b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6fa3c5cd2dc7efbe15a2f1d888e8791819023b0d21ae4de3f8014b6b7cf2be10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62205270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa63ff55c40363d84978d0bd4f41d56d7d4bf4b33a7ea1f30d94b6a0dce6323`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f3585a47bc028e750f37684bbf67de38d2c5ae102b8742405c4fa2364647863a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63828887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba048c8ea90cafeac8f911ba460a0a6924d8d056a9caf220a8628458a5f6ba77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:21693ea27108e5514cd3fce013a53ea08b32e2ad6dd9d3263f38bf9c3bab6e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:482a94c2fbb091d98d5f458dad127758f4774d6c850386b8e9f637099fa92463
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.3 MB (485327027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4553ac9cb419bbc8bf2268c081472d5ef9ae180c2f978ef628deed7ca6fa414`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:26:52 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-3c9668ec048dfa6db814960c8f21d657525398c311820322e74a0cd5c740a565.tar.gz"  && echo "28f895ddb81eab8d861e7f1adc7c54a47146dc14956644e699d4eb9ead29f515  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49cb7dc0d9e4a04a4e0043db8324496b140ebf112a0615b6975552ed5e9f9a`  
		Last Modified: Fri, 18 Mar 2022 05:28:47 GMT  
		Size: 423.1 MB (423121757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:eb66bea13e8eb8b6402f2396470190f5201029f1740f7571511d66fdd157dcdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2615f7bdf3f4ddc681610c299da2d5c5c1dfb862ccb4e2f3c5ff0558c98ff73f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:23 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-3c9668ec048dfa6db814960c8f21d657525398c311820322e74a0cd5c740a565.tar.gz"  && echo "28f895ddb81eab8d861e7f1adc7c54a47146dc14956644e699d4eb9ead29f515  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cd7a9d9c15edb2f1e103b9fc3acb6251a5ee9d252dae649c8d9c61b88973b5`  
		Last Modified: Fri, 18 Mar 2022 00:39:16 GMT  
		Size: 423.1 MB (423121720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
