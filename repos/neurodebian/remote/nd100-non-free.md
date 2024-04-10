## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:5a5f2e3d774ccaa673ced31bebf2a21feb56d490ce9f34351ef4a0869944338a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:46caa95c7eb720464d75c3953707cca21cb3e7122fd2f77564cb8dabb0b3d6b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61307304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449371d9516fa34da70eea0e534127b9c95e0b34a8879e1f7e4f47db45aa036f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:53:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:53:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Mar 2024 02:53:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Mar 2024 02:53:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:53:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef77e55cd43c6390530fae413adcfadfb812b57845a66b2ba04928a1a9abb8`  
		Last Modified: Tue, 12 Mar 2024 02:55:23 GMT  
		Size: 10.5 MB (10504669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9b6aac46ab5b8e6ff1c2d7da8220af4325931d5578214caef0333dab6b453c`  
		Last Modified: Tue, 12 Mar 2024 02:55:22 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a5aa62c4cab45427ffe6c5c64280331c79966e4698bbd694f24bb3938f0425`  
		Last Modified: Tue, 12 Mar 2024 02:55:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7970e6dabfa5b252b9b7e637d09b7cfacf9ef3f5148bb77c23191462a606d45`  
		Last Modified: Tue, 12 Mar 2024 02:55:22 GMT  
		Size: 299.5 KB (299472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1d19aa53782c890d66eaf0ff24747e347d1a6b869cff8800c23bc63f1c06b`  
		Last Modified: Tue, 12 Mar 2024 02:55:30 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:df8d4b80d45b443bbbd057c6c9bf5b1c3de3a4d96c4597de3c0241db1f89cabc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60103346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bb49e565e081db4a8b6a3a57a5d377935756b93961e76defcf2bd605d6c006`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c4757334e56405db1c09af06445ba3f4fcdba0bc1a3a6aa6dedc3e8d35f12`  
		Last Modified: Wed, 10 Apr 2024 07:25:28 GMT  
		Size: 10.5 MB (10510652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42864a2664dfac5044b413d948c7888d5c44ce7f01329029144314f0a8e0511`  
		Last Modified: Wed, 10 Apr 2024 07:25:27 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0796eb6e9f77c0792b97bee5381ecd0eb657527e424ebee0c1ab42234b5577`  
		Last Modified: Wed, 10 Apr 2024 07:25:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308ec07ba36d3e97ce528ff105206526ec927f53a797cf3ead8166924aea0374`  
		Last Modified: Wed, 10 Apr 2024 07:25:27 GMT  
		Size: 299.5 KB (299497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a3cb3e27c5a478969d0eef980722b69c7d2d5f22a0be1d67e809b8a9d1071e`  
		Last Modified: Wed, 10 Apr 2024 07:25:36 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1e087e0531fce17fec3203a4fd3db9132ac8d0c52841365772e1d34f11240896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1050ab7f1f273d04e2de05d45259b5682c474d7e8e6e169e125a43ecfd38c5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:45 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Wed, 10 Apr 2024 00:57:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:22:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:22:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:22:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8784b17322d3d4a6b07cd237ba7efe07278b1e0c9664aeb2629fb4549a858a9`  
		Last Modified: Wed, 10 Apr 2024 07:24:35 GMT  
		Size: 10.9 MB (10868462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af86fdf824835b62c3d8705ea2f6349a655a9d7694f6d4db4c9457ee449df8f`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83b62197ab09a16810d259602f4d31d648b49ae6f812ffbe3a4534056145bf2`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4c400e7b23507419bdb5153ffe01fa0ce304a6f128930f4809da6f69701d1b`  
		Last Modified: Wed, 10 Apr 2024 07:24:34 GMT  
		Size: 299.4 KB (299396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c99c77dd89a66b028c71d03c07e750f68bfa1381a67c00d6f99b44569556ed`  
		Last Modified: Wed, 10 Apr 2024 07:24:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
