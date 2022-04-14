<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20220406.1`](#amazonlinux20202204061)
-	[`amazonlinux:2.0.20220406.1-with-sources`](#amazonlinux20202204061-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20220315.0`](#amazonlinux2018030202203150)
-	[`amazonlinux:2018.03.0.20220315.0-with-sources`](#amazonlinux2018030202203150-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20220315.0`](#amazonlinux20220202203150)
-	[`amazonlinux:2022.0.20220315.0-with-sources`](#amazonlinux20220202203150-with-sources)
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
$ docker pull amazonlinux@sha256:c17c510a1d927c7bf461ada9d80d0131f926ecd1ca07ffa3b1aa7fc0be15bc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f8baf57c1fa876fb816cdefde432a5771d977ed013bff28a61ce8c28aea7837d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62237641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41faacb0c5135c876cd2bf95bfd50afbc5817f7f12cddc9d6463f93267826f54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:147beb6594d3665f97fa62af8668901097c60f71ae85484e4478e2816a001f03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63870281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53695f051b33dec81ea4dbf4b4450dcfaad841774c016f26290d14c8879d33a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:2fb42dead48615005ba5025a4fbbf78e727a109db62e2bf4983458d75df5275c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:10ab75802dd29ae735c049114c2b611129bb94ce07362f026057bc10a4b5ba0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485466953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627a04a8a008d782bc28123d6dbdafa6f3f8afd131c672ff0a00e23f430334a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:26:30 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a46ccefa1703a8b084ff61437d3d05b29f0a2c6eb6ec89bd30e032b170f7dd2`  
		Last Modified: Wed, 13 Apr 2022 21:27:38 GMT  
		Size: 423.2 MB (423229312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:1773bdac84c234a2f6c22851691bddccaaf1840e23b3c2b03872ef1a8cfebdac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4bdce10b7213f190095856d33f28b129c6f0858ba3ff1f73161425e84abad3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:39:50 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06ba8c8fdc0b7272b7bef0ff89656b50b63e5b4baddfa8bda2b42d73a7ebc1d`  
		Last Modified: Wed, 13 Apr 2022 21:41:23 GMT  
		Size: 423.2 MB (423229256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220406.1`

```console
$ docker pull amazonlinux@sha256:c17c510a1d927c7bf461ada9d80d0131f926ecd1ca07ffa3b1aa7fc0be15bc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220406.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f8baf57c1fa876fb816cdefde432a5771d977ed013bff28a61ce8c28aea7837d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62237641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41faacb0c5135c876cd2bf95bfd50afbc5817f7f12cddc9d6463f93267826f54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220406.1` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:147beb6594d3665f97fa62af8668901097c60f71ae85484e4478e2816a001f03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63870281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53695f051b33dec81ea4dbf4b4450dcfaad841774c016f26290d14c8879d33a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220406.1-with-sources`

```console
$ docker pull amazonlinux@sha256:2fb42dead48615005ba5025a4fbbf78e727a109db62e2bf4983458d75df5275c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220406.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:10ab75802dd29ae735c049114c2b611129bb94ce07362f026057bc10a4b5ba0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485466953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627a04a8a008d782bc28123d6dbdafa6f3f8afd131c672ff0a00e23f430334a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:26:30 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a46ccefa1703a8b084ff61437d3d05b29f0a2c6eb6ec89bd30e032b170f7dd2`  
		Last Modified: Wed, 13 Apr 2022 21:27:38 GMT  
		Size: 423.2 MB (423229312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220406.1-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:1773bdac84c234a2f6c22851691bddccaaf1840e23b3c2b03872ef1a8cfebdac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4bdce10b7213f190095856d33f28b129c6f0858ba3ff1f73161425e84abad3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:39:50 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06ba8c8fdc0b7272b7bef0ff89656b50b63e5b4baddfa8bda2b42d73a7ebc1d`  
		Last Modified: Wed, 13 Apr 2022 21:41:23 GMT  
		Size: 423.2 MB (423229256 bytes)  
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
$ docker pull amazonlinux@sha256:b43e6145a7c17c628533cf743fe1555eb0766f91067ba13546d32fb832dd0a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c74e77c670519cd69e3f5ce3fa714c02c582a40d786dd7e97113e717e7655e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70551902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596c538642b7e6e4555a5995097d5b9d754a024d98026531b8b8398ffd920296`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 22:06:49 GMT
ADD file:0e00ccd2daf7fcbf2c4b6c87fc4c7426cb4744220d4688380b712b0a10b1ce17 in / 
# Wed, 30 Mar 2022 22:06:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51621d34d545ca53a75f5f765d89feed132eed23e837845dab564cd60d3c4a8d`  
		Last Modified: Wed, 30 Mar 2022 22:07:49 GMT  
		Size: 70.6 MB (70551902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:dde8762c9c365a36934cb4f000ed611c19e52b8c5e32ea0d51a4672029ecdbf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69106021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afd7915f681cff0714f53daa5fdacc9983b5e0e06b2c0bac438e6421724843c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 18:25:19 GMT
ADD file:b4343bb7616f343b9a7343c7512a69010bd7f36e2c2e218e0eea2f57382746cf in / 
# Wed, 30 Mar 2022 18:25:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1539c116c8b0d4e18a17732583c333362ac930b6eb4be2833fff8a8ab2ea6b8b`  
		Last Modified: Wed, 30 Mar 2022 18:26:53 GMT  
		Size: 69.1 MB (69106021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:c7b999c4dafbef559f121d77f919a775db13ddcea68a31d846b4d3e9ef317469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2fb367b85dcc2797239921217f62d98c66b4e614609ae8130d85ea12fa2be3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.1 MB (489146951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572b53c2976082cbb5f61cdd5677e4d8f173f835f7f46f692f85743b824f0c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 22:06:49 GMT
ADD file:0e00ccd2daf7fcbf2c4b6c87fc4c7426cb4744220d4688380b712b0a10b1ce17 in / 
# Wed, 30 Mar 2022 22:06:49 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 22:07:13 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-feddddadaa0ca95e9807903d234b2e9192782e81abe4ae95c969d9acf5d1a223.tar.gz"  && echo "a2450fe78ed3b89a144721743a282fcb5041783247ae040872007c08d36a83e1  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:51621d34d545ca53a75f5f765d89feed132eed23e837845dab564cd60d3c4a8d`  
		Last Modified: Wed, 30 Mar 2022 22:07:49 GMT  
		Size: 70.6 MB (70551902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4592a6a3eb2786610fec5f2359858c714b4968d2e854cde2a0adedbc33b2cf`  
		Last Modified: Wed, 30 Mar 2022 22:08:17 GMT  
		Size: 418.6 MB (418595049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:e2dd86254b03868c5c0566669f828081a230149217b93dedce7902ae792d910f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487701029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15709e43976d58175cbdcb7b62bb8d5a6a1b1618c7ba82580e570e92909e68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 18:25:19 GMT
ADD file:b4343bb7616f343b9a7343c7512a69010bd7f36e2c2e218e0eea2f57382746cf in / 
# Wed, 30 Mar 2022 18:25:20 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 18:26:04 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-feddddadaa0ca95e9807903d234b2e9192782e81abe4ae95c969d9acf5d1a223.tar.gz"  && echo "a2450fe78ed3b89a144721743a282fcb5041783247ae040872007c08d36a83e1  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:1539c116c8b0d4e18a17732583c333362ac930b6eb4be2833fff8a8ab2ea6b8b`  
		Last Modified: Wed, 30 Mar 2022 18:26:53 GMT  
		Size: 69.1 MB (69106021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51ff1c75bc99c531f890a7b86060bf09ced222193f634e9f1b029ae55afb22c`  
		Last Modified: Wed, 30 Mar 2022 18:27:28 GMT  
		Size: 418.6 MB (418595008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220315.0`

```console
$ docker pull amazonlinux@sha256:b43e6145a7c17c628533cf743fe1555eb0766f91067ba13546d32fb832dd0a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220315.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c74e77c670519cd69e3f5ce3fa714c02c582a40d786dd7e97113e717e7655e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70551902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596c538642b7e6e4555a5995097d5b9d754a024d98026531b8b8398ffd920296`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 22:06:49 GMT
ADD file:0e00ccd2daf7fcbf2c4b6c87fc4c7426cb4744220d4688380b712b0a10b1ce17 in / 
# Wed, 30 Mar 2022 22:06:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51621d34d545ca53a75f5f765d89feed132eed23e837845dab564cd60d3c4a8d`  
		Last Modified: Wed, 30 Mar 2022 22:07:49 GMT  
		Size: 70.6 MB (70551902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220315.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:dde8762c9c365a36934cb4f000ed611c19e52b8c5e32ea0d51a4672029ecdbf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69106021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afd7915f681cff0714f53daa5fdacc9983b5e0e06b2c0bac438e6421724843c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 18:25:19 GMT
ADD file:b4343bb7616f343b9a7343c7512a69010bd7f36e2c2e218e0eea2f57382746cf in / 
# Wed, 30 Mar 2022 18:25:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1539c116c8b0d4e18a17732583c333362ac930b6eb4be2833fff8a8ab2ea6b8b`  
		Last Modified: Wed, 30 Mar 2022 18:26:53 GMT  
		Size: 69.1 MB (69106021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220315.0-with-sources`

```console
$ docker pull amazonlinux@sha256:c7b999c4dafbef559f121d77f919a775db13ddcea68a31d846b4d3e9ef317469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220315.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2fb367b85dcc2797239921217f62d98c66b4e614609ae8130d85ea12fa2be3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.1 MB (489146951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572b53c2976082cbb5f61cdd5677e4d8f173f835f7f46f692f85743b824f0c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 22:06:49 GMT
ADD file:0e00ccd2daf7fcbf2c4b6c87fc4c7426cb4744220d4688380b712b0a10b1ce17 in / 
# Wed, 30 Mar 2022 22:06:49 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 22:07:13 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-feddddadaa0ca95e9807903d234b2e9192782e81abe4ae95c969d9acf5d1a223.tar.gz"  && echo "a2450fe78ed3b89a144721743a282fcb5041783247ae040872007c08d36a83e1  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:51621d34d545ca53a75f5f765d89feed132eed23e837845dab564cd60d3c4a8d`  
		Last Modified: Wed, 30 Mar 2022 22:07:49 GMT  
		Size: 70.6 MB (70551902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4592a6a3eb2786610fec5f2359858c714b4968d2e854cde2a0adedbc33b2cf`  
		Last Modified: Wed, 30 Mar 2022 22:08:17 GMT  
		Size: 418.6 MB (418595049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220315.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:e2dd86254b03868c5c0566669f828081a230149217b93dedce7902ae792d910f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487701029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15709e43976d58175cbdcb7b62bb8d5a6a1b1618c7ba82580e570e92909e68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 18:25:19 GMT
ADD file:b4343bb7616f343b9a7343c7512a69010bd7f36e2c2e218e0eea2f57382746cf in / 
# Wed, 30 Mar 2022 18:25:20 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 18:26:04 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-feddddadaa0ca95e9807903d234b2e9192782e81abe4ae95c969d9acf5d1a223.tar.gz"  && echo "a2450fe78ed3b89a144721743a282fcb5041783247ae040872007c08d36a83e1  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:1539c116c8b0d4e18a17732583c333362ac930b6eb4be2833fff8a8ab2ea6b8b`  
		Last Modified: Wed, 30 Mar 2022 18:26:53 GMT  
		Size: 69.1 MB (69106021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51ff1c75bc99c531f890a7b86060bf09ced222193f634e9f1b029ae55afb22c`  
		Last Modified: Wed, 30 Mar 2022 18:27:28 GMT  
		Size: 418.6 MB (418595008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:b43e6145a7c17c628533cf743fe1555eb0766f91067ba13546d32fb832dd0a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c74e77c670519cd69e3f5ce3fa714c02c582a40d786dd7e97113e717e7655e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70551902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596c538642b7e6e4555a5995097d5b9d754a024d98026531b8b8398ffd920296`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 22:06:49 GMT
ADD file:0e00ccd2daf7fcbf2c4b6c87fc4c7426cb4744220d4688380b712b0a10b1ce17 in / 
# Wed, 30 Mar 2022 22:06:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51621d34d545ca53a75f5f765d89feed132eed23e837845dab564cd60d3c4a8d`  
		Last Modified: Wed, 30 Mar 2022 22:07:49 GMT  
		Size: 70.6 MB (70551902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:dde8762c9c365a36934cb4f000ed611c19e52b8c5e32ea0d51a4672029ecdbf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69106021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afd7915f681cff0714f53daa5fdacc9983b5e0e06b2c0bac438e6421724843c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 18:25:19 GMT
ADD file:b4343bb7616f343b9a7343c7512a69010bd7f36e2c2e218e0eea2f57382746cf in / 
# Wed, 30 Mar 2022 18:25:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1539c116c8b0d4e18a17732583c333362ac930b6eb4be2833fff8a8ab2ea6b8b`  
		Last Modified: Wed, 30 Mar 2022 18:26:53 GMT  
		Size: 69.1 MB (69106021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:c7b999c4dafbef559f121d77f919a775db13ddcea68a31d846b4d3e9ef317469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2fb367b85dcc2797239921217f62d98c66b4e614609ae8130d85ea12fa2be3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.1 MB (489146951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572b53c2976082cbb5f61cdd5677e4d8f173f835f7f46f692f85743b824f0c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 22:06:49 GMT
ADD file:0e00ccd2daf7fcbf2c4b6c87fc4c7426cb4744220d4688380b712b0a10b1ce17 in / 
# Wed, 30 Mar 2022 22:06:49 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 22:07:13 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-feddddadaa0ca95e9807903d234b2e9192782e81abe4ae95c969d9acf5d1a223.tar.gz"  && echo "a2450fe78ed3b89a144721743a282fcb5041783247ae040872007c08d36a83e1  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:51621d34d545ca53a75f5f765d89feed132eed23e837845dab564cd60d3c4a8d`  
		Last Modified: Wed, 30 Mar 2022 22:07:49 GMT  
		Size: 70.6 MB (70551902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4592a6a3eb2786610fec5f2359858c714b4968d2e854cde2a0adedbc33b2cf`  
		Last Modified: Wed, 30 Mar 2022 22:08:17 GMT  
		Size: 418.6 MB (418595049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:e2dd86254b03868c5c0566669f828081a230149217b93dedce7902ae792d910f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487701029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15709e43976d58175cbdcb7b62bb8d5a6a1b1618c7ba82580e570e92909e68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Mar 2022 18:25:19 GMT
ADD file:b4343bb7616f343b9a7343c7512a69010bd7f36e2c2e218e0eea2f57382746cf in / 
# Wed, 30 Mar 2022 18:25:20 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 18:26:04 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-feddddadaa0ca95e9807903d234b2e9192782e81abe4ae95c969d9acf5d1a223.tar.gz"  && echo "a2450fe78ed3b89a144721743a282fcb5041783247ae040872007c08d36a83e1  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:1539c116c8b0d4e18a17732583c333362ac930b6eb4be2833fff8a8ab2ea6b8b`  
		Last Modified: Wed, 30 Mar 2022 18:26:53 GMT  
		Size: 69.1 MB (69106021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51ff1c75bc99c531f890a7b86060bf09ced222193f634e9f1b029ae55afb22c`  
		Last Modified: Wed, 30 Mar 2022 18:27:28 GMT  
		Size: 418.6 MB (418595008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:c17c510a1d927c7bf461ada9d80d0131f926ecd1ca07ffa3b1aa7fc0be15bc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f8baf57c1fa876fb816cdefde432a5771d977ed013bff28a61ce8c28aea7837d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62237641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41faacb0c5135c876cd2bf95bfd50afbc5817f7f12cddc9d6463f93267826f54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:147beb6594d3665f97fa62af8668901097c60f71ae85484e4478e2816a001f03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63870281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53695f051b33dec81ea4dbf4b4450dcfaad841774c016f26290d14c8879d33a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:2fb42dead48615005ba5025a4fbbf78e727a109db62e2bf4983458d75df5275c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:10ab75802dd29ae735c049114c2b611129bb94ce07362f026057bc10a4b5ba0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485466953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627a04a8a008d782bc28123d6dbdafa6f3f8afd131c672ff0a00e23f430334a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:26:30 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a46ccefa1703a8b084ff61437d3d05b29f0a2c6eb6ec89bd30e032b170f7dd2`  
		Last Modified: Wed, 13 Apr 2022 21:27:38 GMT  
		Size: 423.2 MB (423229312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:1773bdac84c234a2f6c22851691bddccaaf1840e23b3c2b03872ef1a8cfebdac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4bdce10b7213f190095856d33f28b129c6f0858ba3ff1f73161425e84abad3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:39:50 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06ba8c8fdc0b7272b7bef0ff89656b50b63e5b4baddfa8bda2b42d73a7ebc1d`  
		Last Modified: Wed, 13 Apr 2022 21:41:23 GMT  
		Size: 423.2 MB (423229256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
