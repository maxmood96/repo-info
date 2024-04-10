## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:a8919f6d0b5f1c4652d275cf1f12eb4e3bbd5ac9ece043057cc12bd47959bac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:745c4c59eb3122aaf5dcdedcef53dc748a606f7ec3ff3ef7048cc75bca8c8d31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d82aef271ab6f7dc51aa3f559c3eda72c2f1f1577f5d24f76f678eea816c1a`
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

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1615c3ce9446cdb0712e4213ff32eda3958841059f2a04c89dfa29c61c638d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60102986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37cde3a633fbe59f4d3b0f7fb11197dc358f3ba30f7eedfbdb977030e9e6b5`
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

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:df8d03c48e83e5849a8fd395a81f6a24395968e77bb2c98d032044ead1c64962
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9966b92f65077c736ffdee2928aef16b1a12949a00c6670f6bbde84d1f147b13`
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
