## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:7d9413828fa6db511e9a25ea68b40eefebcfefb3988f9722e0447932a0c14058
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
$ docker pull debian@sha256:246ecc7e9071d2055116e3f6770d481e3f002d3abbbf6f8a1ee9158a88e2dd2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f15e0ab0910dcb9be15483877659610527eeadf6f2aa527e57b4503b10dcbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:26 GMT
ADD file:ce04d6a354feaef93795269c859f36667fce9efda23c61b37d7060263b66ed4e in / 
# Wed, 20 Sep 2023 04:55:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:55:33 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:167b8a53ca4504bc6aa3182e336fa96f4ef76875d158c1933d3e2fa19c57e0c3`  
		Last Modified: Wed, 20 Sep 2023 04:59:55 GMT  
		Size: 49.6 MB (49557601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6e5a7d2e4374a0c040fb3822a5903f6238f077399234c95d2da52b684875f6`  
		Last Modified: Wed, 20 Sep 2023 05:00:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2dffad9c1ae6eb4eec8c9ee333666cdbbb89dffa851b7f434598e663594640ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47415238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fc41ca4a34bd0344f7df3afae3eee7fff709fbbe1b89f586680d311278562f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:41 GMT
ADD file:4c262e2fcc04b6144cc529b2b0dbd984b5f44ecf09bd87707631cb5cad3012f0 in / 
# Wed, 20 Sep 2023 00:49:42 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:49:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c2e728ebba2eb6503d5975d2d8245f959ffad36ab8a83164e1c7e45956c36080`  
		Last Modified: Wed, 20 Sep 2023 00:54:16 GMT  
		Size: 47.4 MB (47415014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8d8a9d04d9d14202bceabafde12dec5e7cb8fb8bb24ea4f1364cd7f1788220`  
		Last Modified: Wed, 20 Sep 2023 00:54:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0134b65b2d8025477d5973c8055ac5dd58a56747367851a565b86df19911c996
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19b98d16ad12fd62276c74a29777948c6ae1b5ac8f7047cd81c1aa81e92cb61`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:08 GMT
ADD file:e8c98b19a39772b96a8bfa0f38abfc620498f040012f9b9906640975ac01ce0d in / 
# Wed, 20 Sep 2023 04:57:09 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:57:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:013e3017888216ce95d0ffe3d0fb039c509402dc99800465157f56e7520abd4a`  
		Last Modified: Wed, 20 Sep 2023 05:00:53 GMT  
		Size: 45.2 MB (45232576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d3c58cde2d306b7941bddd33dace0cf895895ae5b953d1a72a789e9d03982a`  
		Last Modified: Wed, 20 Sep 2023 05:01:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ba33d95a6850713ea4d587982a551d72fca0ffad67ca36146fb9a2d2c6a51a7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49592106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef42486ce0c413ea47c9e10968a58e023d1e450474947565facd6e595812e4ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:04 GMT
ADD file:7a0adbde6e967e2bcaafa69f04fabdec993025645c8d0d51acc991a31b404eed in / 
# Wed, 20 Sep 2023 02:44:05 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:44:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:796cc43785ac3cd0081892bd48e545a0615415265b60c794fdf81ac95b034213`  
		Last Modified: Wed, 20 Sep 2023 02:47:15 GMT  
		Size: 49.6 MB (49591881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbf6546f13b44d67daf377244a2dc836e027ede713363a6000b0325cbd1fc00`  
		Last Modified: Wed, 20 Sep 2023 02:47:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:f68d0c4a15f3ecd988ebfdad10ba5bcd0653545f01f74d4fc08ad4bb5e934f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50569190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b789b1febd20a397fcc0e922b491245db9a0b69a1428ee8f39ed8d051c528c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:41:42 GMT
ADD file:23c52eb6ca90f95eb3fff17deef5cfb900f1807fd50deae367183075f49aa81d in / 
# Wed, 20 Sep 2023 00:41:45 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:41:48 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b3de420baafed4c606a756da9f1ab4e930a007eb8cb0a1104bc280c0b7820cbf`  
		Last Modified: Wed, 20 Sep 2023 00:46:20 GMT  
		Size: 50.6 MB (50568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5809cb2ea2d59b61bd601acaf1dc5a2e2cb17af634ede427a4695795717952f5`  
		Last Modified: Wed, 20 Sep 2023 00:46:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e3649ff5455003194710471e3ef4b66ac1da2883684883c498e3b639ab6d013f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ef8ebe395f9a5c36843d1a595ef0035422502202c851488b0345a4870a974f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:09:14 GMT
ADD file:fcce6589274e33563988a8b5cf9be10cd70df7b83bdf6713a5162f272a6c801f in / 
# Wed, 20 Sep 2023 03:09:19 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 03:09:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d60e76f86e60c0c2ec7b83df437d97bc329aab62315d63446e73d0ccc6bed0b5`  
		Last Modified: Wed, 20 Sep 2023 03:20:16 GMT  
		Size: 49.5 MB (49542389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def2ab52103fe835b153e626d72b599e27b890ac597d60e8c67c5851164a9cf6`  
		Last Modified: Wed, 20 Sep 2023 03:20:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:03d1df336ca21710472ee0ea3c6df60f29b56a33a9a26c92dd0e7502fa5bed01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53545023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bf915f97e56bb476e5d5500648ad49f40c4b353a9a7088774d4658bc9c8cdb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 07:52:31 GMT
ADD file:dc6a80175c6d467f50c4ff816701171cd27bd98fc9bb7292161e476ada0cfed1 in / 
# Wed, 20 Sep 2023 07:52:34 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:52:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dacd41a2ee8a7a272473dd20943e3e5c0ddac0964f5610239dd5ae6c807c000c`  
		Last Modified: Wed, 20 Sep 2023 08:49:21 GMT  
		Size: 53.5 MB (53544796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d70fba54ffbd7761ec3b405f1357fb978df0baa45b26a64fe1296d491720713`  
		Last Modified: Wed, 20 Sep 2023 08:49:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:5e31a82923513f25f033f234e8061431169e9292c9576ef36d836d49e2fdeaea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47921994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298eab8de67be1cd92e6e36e602767b32171788449b887d134fdb91710ac5946`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:09 GMT
ADD file:988f82e85974ad63522cfbd8ca56dddd8dd9825ed628600e9a5037d77d1bd890 in / 
# Wed, 20 Sep 2023 02:54:12 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:54:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca5551f4914a3e8f0c34772f4d772442cbf259e6ee48db35d827776924e556bf`  
		Last Modified: Wed, 20 Sep 2023 02:59:30 GMT  
		Size: 47.9 MB (47921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d760c2fe4b13d6eb64bb50b52b0d35eb900c99942bc547cf1ba23f9bef531da`  
		Last Modified: Wed, 20 Sep 2023 02:59:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
