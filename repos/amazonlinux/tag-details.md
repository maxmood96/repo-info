<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03.0.20210126.1`](#amazonlinux2018030202101261)
-	[`amazonlinux:2018.03.0.20210126.1-with-sources`](#amazonlinux2018030202101261-with-sources)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2.0.20210126.0`](#amazonlinux20202101260)
-	[`amazonlinux:2.0.20210126.0-with-sources`](#amazonlinux20202101260-with-sources)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:9bd78c849b25ff2367dfdc1341cb30a7918db0bb452a1373afc37722559fabe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:4608bf17c7b691c5a81ae7f599631055bce8bd5ad8b43e85613c00802ef05ec7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62221008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68556ba4ccd0c17cb55f71a283997e5e2b4c85ce2a17318af297411a426be024`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:20:25 GMT
ADD file:0e86c898f076c0be7554fa629ffd98f1581cc0aeadd702b3876c03b300495006 in / 
# Wed, 27 Jan 2021 22:20:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a441db1e9917658028bdaa8d10a00f6d24aa1f4de352b6b3d327b627207845db`  
		Last Modified: Wed, 27 Jan 2021 22:22:10 GMT  
		Size: 62.2 MB (62221008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:61b78057f1b5b75be20e3e904e60e157dfd51c4112ffef53b607f83c6261fe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2a59ee8b4934195156ba8b6b4539d632dd8f79b598747a54a08c9122d58cb3dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449079131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57cdbc7f9d8a3e4fd1dc16736e612142f013423d3ec448d21dd8c8d8db0bb53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:20:25 GMT
ADD file:0e86c898f076c0be7554fa629ffd98f1581cc0aeadd702b3876c03b300495006 in / 
# Wed, 27 Jan 2021 22:20:25 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:49 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c05e579179c56d65b75577c4714e241c43b021f6c5595e79ec5f5d693c3e697c.tar.gz"  && echo "a5a576edc920ac864f63ecd88bca4eeeeea9721653e7f1b2eba858721057e122  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a441db1e9917658028bdaa8d10a00f6d24aa1f4de352b6b3d327b627207845db`  
		Last Modified: Wed, 27 Jan 2021 22:22:10 GMT  
		Size: 62.2 MB (62221008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cfd22c9150a319ed2655cf628b2d5725a7a4704a2ed9003798ea147e02057`  
		Last Modified: Wed, 27 Jan 2021 22:22:33 GMT  
		Size: 386.9 MB (386858123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:916aa32ef5814bee62736fcb7d58355164a69c7605d58781379d985eb252b629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3c663506cf84b035d68c6450c48f76092821736d6b0615d8bd45f3caf525abe7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61996576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79e41188c15ef69321ebdd86af0e1e68be4c3b03c4c4ff418900fd70a90a9db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:d4e6ef65af9890813147ffac08f349a0d0c1edbe840d3fd0430723f63f73a78c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63707914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29a7714b76a8ac87a5634269fb63b50c709bc940cc096d773d565d67218c29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:9bd78c849b25ff2367dfdc1341cb30a7918db0bb452a1373afc37722559fabe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:4608bf17c7b691c5a81ae7f599631055bce8bd5ad8b43e85613c00802ef05ec7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62221008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68556ba4ccd0c17cb55f71a283997e5e2b4c85ce2a17318af297411a426be024`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:20:25 GMT
ADD file:0e86c898f076c0be7554fa629ffd98f1581cc0aeadd702b3876c03b300495006 in / 
# Wed, 27 Jan 2021 22:20:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a441db1e9917658028bdaa8d10a00f6d24aa1f4de352b6b3d327b627207845db`  
		Last Modified: Wed, 27 Jan 2021 22:22:10 GMT  
		Size: 62.2 MB (62221008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210126.1`

```console
$ docker pull amazonlinux@sha256:9bd78c849b25ff2367dfdc1341cb30a7918db0bb452a1373afc37722559fabe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20210126.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:4608bf17c7b691c5a81ae7f599631055bce8bd5ad8b43e85613c00802ef05ec7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62221008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68556ba4ccd0c17cb55f71a283997e5e2b4c85ce2a17318af297411a426be024`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:20:25 GMT
ADD file:0e86c898f076c0be7554fa629ffd98f1581cc0aeadd702b3876c03b300495006 in / 
# Wed, 27 Jan 2021 22:20:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a441db1e9917658028bdaa8d10a00f6d24aa1f4de352b6b3d327b627207845db`  
		Last Modified: Wed, 27 Jan 2021 22:22:10 GMT  
		Size: 62.2 MB (62221008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210126.1-with-sources`

```console
$ docker pull amazonlinux@sha256:61b78057f1b5b75be20e3e904e60e157dfd51c4112ffef53b607f83c6261fe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20210126.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2a59ee8b4934195156ba8b6b4539d632dd8f79b598747a54a08c9122d58cb3dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449079131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57cdbc7f9d8a3e4fd1dc16736e612142f013423d3ec448d21dd8c8d8db0bb53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:20:25 GMT
ADD file:0e86c898f076c0be7554fa629ffd98f1581cc0aeadd702b3876c03b300495006 in / 
# Wed, 27 Jan 2021 22:20:25 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:49 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c05e579179c56d65b75577c4714e241c43b021f6c5595e79ec5f5d693c3e697c.tar.gz"  && echo "a5a576edc920ac864f63ecd88bca4eeeeea9721653e7f1b2eba858721057e122  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a441db1e9917658028bdaa8d10a00f6d24aa1f4de352b6b3d327b627207845db`  
		Last Modified: Wed, 27 Jan 2021 22:22:10 GMT  
		Size: 62.2 MB (62221008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cfd22c9150a319ed2655cf628b2d5725a7a4704a2ed9003798ea147e02057`  
		Last Modified: Wed, 27 Jan 2021 22:22:33 GMT  
		Size: 386.9 MB (386858123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:61b78057f1b5b75be20e3e904e60e157dfd51c4112ffef53b607f83c6261fe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2a59ee8b4934195156ba8b6b4539d632dd8f79b598747a54a08c9122d58cb3dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449079131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57cdbc7f9d8a3e4fd1dc16736e612142f013423d3ec448d21dd8c8d8db0bb53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:20:25 GMT
ADD file:0e86c898f076c0be7554fa629ffd98f1581cc0aeadd702b3876c03b300495006 in / 
# Wed, 27 Jan 2021 22:20:25 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:49 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c05e579179c56d65b75577c4714e241c43b021f6c5595e79ec5f5d693c3e697c.tar.gz"  && echo "a5a576edc920ac864f63ecd88bca4eeeeea9721653e7f1b2eba858721057e122  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a441db1e9917658028bdaa8d10a00f6d24aa1f4de352b6b3d327b627207845db`  
		Last Modified: Wed, 27 Jan 2021 22:22:10 GMT  
		Size: 62.2 MB (62221008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cfd22c9150a319ed2655cf628b2d5725a7a4704a2ed9003798ea147e02057`  
		Last Modified: Wed, 27 Jan 2021 22:22:33 GMT  
		Size: 386.9 MB (386858123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210126.0`

```console
$ docker pull amazonlinux@sha256:679f35af8b1ac7d78190e79af3be4d0fd1ea45641280373fe76f438a5732608b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2.0.20210126.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3c663506cf84b035d68c6450c48f76092821736d6b0615d8bd45f3caf525abe7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61996576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79e41188c15ef69321ebdd86af0e1e68be4c3b03c4c4ff418900fd70a90a9db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210126.0-with-sources`

```console
$ docker pull amazonlinux@sha256:dab986a6faa214c240d69a9fcacd4fa2621bacbaf86deaef1e67a9fd48f6d3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2.0.20210126.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:983d3e4de81b1c27d66e23dcaa8a16c475d5c5b495aa385604ccb648a8058788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542850367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e352e313d08efc3970e6993a06e67920b041e2e9e87622b5a62639aee5437d5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:10 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-020afd68ea87fb6a4b381a6874ce0c38c6f291f66d9f9d9fda853a9bc76a954d.tar.gz"  && echo "c74f4742eb862e351271e7bceff838061332d4bba919f1944568ed779351fceb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332009c39171868832b64d8784eba0fb853d50be1faf582791d991cf57a9210f`  
		Last Modified: Wed, 27 Jan 2021 22:21:53 GMT  
		Size: 480.9 MB (480853791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:150721a0226b49f11ccd47ff3af21495abed1ac0e53f835222330565ae55d84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:983d3e4de81b1c27d66e23dcaa8a16c475d5c5b495aa385604ccb648a8058788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542850367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e352e313d08efc3970e6993a06e67920b041e2e9e87622b5a62639aee5437d5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:10 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-020afd68ea87fb6a4b381a6874ce0c38c6f291f66d9f9d9fda853a9bc76a954d.tar.gz"  && echo "c74f4742eb862e351271e7bceff838061332d4bba919f1944568ed779351fceb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332009c39171868832b64d8784eba0fb853d50be1faf582791d991cf57a9210f`  
		Last Modified: Wed, 27 Jan 2021 22:21:53 GMT  
		Size: 480.9 MB (480853791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:9c7588150eff1d7928416c7fafd35edaa4f1d03d663f0c7fdac8ac62de67c8a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.6 MB (544552541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d28578129bba32d0a61dcb4c5ce73ca3365c60abcae712f3c4d2edd3009ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Wed, 23 Dec 2020 19:40:28 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-826e231a97252a5034e63006e69224de2364211252782ce0d9eab6a50c799006.tar.gz"  && echo "3d237536b5aa360bd744e30abd284cdd42eb182e390f3d4c2abc4655f7a048a2  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3431b17c8d2c281dfa9b3b9f9880a6159a978452bed73137b8af89f04586250c`  
		Last Modified: Wed, 23 Dec 2020 19:41:41 GMT  
		Size: 480.8 MB (480844627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:916aa32ef5814bee62736fcb7d58355164a69c7605d58781379d985eb252b629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3c663506cf84b035d68c6450c48f76092821736d6b0615d8bd45f3caf525abe7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61996576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79e41188c15ef69321ebdd86af0e1e68be4c3b03c4c4ff418900fd70a90a9db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:d4e6ef65af9890813147ffac08f349a0d0c1edbe840d3fd0430723f63f73a78c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63707914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29a7714b76a8ac87a5634269fb63b50c709bc940cc096d773d565d67218c29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:150721a0226b49f11ccd47ff3af21495abed1ac0e53f835222330565ae55d84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:983d3e4de81b1c27d66e23dcaa8a16c475d5c5b495aa385604ccb648a8058788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542850367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e352e313d08efc3970e6993a06e67920b041e2e9e87622b5a62639aee5437d5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:10 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-020afd68ea87fb6a4b381a6874ce0c38c6f291f66d9f9d9fda853a9bc76a954d.tar.gz"  && echo "c74f4742eb862e351271e7bceff838061332d4bba919f1944568ed779351fceb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332009c39171868832b64d8784eba0fb853d50be1faf582791d991cf57a9210f`  
		Last Modified: Wed, 27 Jan 2021 22:21:53 GMT  
		Size: 480.9 MB (480853791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:9c7588150eff1d7928416c7fafd35edaa4f1d03d663f0c7fdac8ac62de67c8a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.6 MB (544552541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d28578129bba32d0a61dcb4c5ce73ca3365c60abcae712f3c4d2edd3009ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Wed, 23 Dec 2020 19:40:28 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-826e231a97252a5034e63006e69224de2364211252782ce0d9eab6a50c799006.tar.gz"  && echo "3d237536b5aa360bd744e30abd284cdd42eb182e390f3d4c2abc4655f7a048a2  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3431b17c8d2c281dfa9b3b9f9880a6159a978452bed73137b8af89f04586250c`  
		Last Modified: Wed, 23 Dec 2020 19:41:41 GMT  
		Size: 480.8 MB (480844627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
