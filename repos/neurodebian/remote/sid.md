## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:abfbc8da1dfc9ff3b545f5d8a864d089d7e8f8936539b57fed63310523815f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:1ecd936078dd03fdfa2fd6c8064cf1a36fd1eef4d36f2c933e001d0ea055e8e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65213287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca526f0ef2949aaa012342d3d6e431c73334d7b42c0d4279ffe7a6d9d02580bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:03:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:03:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5637e2505f3efe6a087f0f58c43c8fa65c0d83fd30901d7560db79c143a89afe`  
		Last Modified: Tue, 21 Nov 2023 09:04:40 GMT  
		Size: 12.8 MB (12802830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bd83037a1745411887e11ab89e62bb031e2361c3db34862b23ca31dee441e1`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ae61a5f7f79b1d181aaba6974a82f53dcc648a239770ffeef958fdfb6a5fb`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536170650855aec71462bc8423f1f5c9bb8c63968ba94830b610238d565d624c`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 286.2 KB (286177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2690b841fc6f042b773a22452f0032c017bf5f60d7c9fa82cca54e48d43ffd74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65155796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339a46c645d8fd2a8bd94d0593950ffc81d4aea42efdef0f976cca50852627c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 16:52:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 16:52:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 16:52:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 16:52:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41e7eb82c5e40582ade62cb8d256dc73d2c41138aebf12a731f9be9125e5d32`  
		Last Modified: Tue, 21 Nov 2023 16:54:11 GMT  
		Size: 15.2 MB (15229505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c1cab5907728d5cc2707ae61e63ed114ae091e4145d4de8ca9596959f9a5da`  
		Last Modified: Tue, 21 Nov 2023 16:54:10 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0bc00e33a83bfb2f58d5fe711e003c5cdb92a1c46cfd43ca939e43a78556f9`  
		Last Modified: Tue, 21 Nov 2023 16:54:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899efab49c99d5d6b1ce7f1e088e8b567a720aa7d276a4ae51ed1a4ead5c46b8`  
		Last Modified: Tue, 21 Nov 2023 16:54:10 GMT  
		Size: 286.5 KB (286481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:ac335da703c703c996fc3e3a992c7f9aceba5899f96e5fdac7c2123b89b57583
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66616111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4039fd99be7369dcf9eae5dba37f6609316594e7f0214124104d48b9224cbf5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:41:31 GMT
ADD file:bfc7d40a1647cd24272e8bfe066e6291b5008d468149e8da8912743fb73ca9d1 in / 
# Tue, 21 Nov 2023 04:41:32 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:31:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:31:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 14:31:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 14:31:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:949c066c0a11d2827a1530818a7ddd8a28c5483bc3fa53f584688eb4a8d87843`  
		Last Modified: Tue, 21 Nov 2023 04:47:52 GMT  
		Size: 50.5 MB (50513831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182b5c261bb2841cbe40eccea3d06d6ae29ec07bbab7906c62e6fac5870ea4f`  
		Last Modified: Tue, 21 Nov 2023 14:33:22 GMT  
		Size: 15.8 MB (15814181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ee0846cd3a515615f86a4f84d28ee1905b0e5152373e2803718696ef9f1c1`  
		Last Modified: Tue, 21 Nov 2023 14:33:20 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64a49d53f3b0bb91225a9b455e0b1a38fc6e97317572314c641cb2e2fa44658`  
		Last Modified: Tue, 21 Nov 2023 14:33:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dcdb49c52ddc53f6fbe10b48b8325990951e4ee8a4ae9d84ae592b34ed006c`  
		Last Modified: Tue, 21 Nov 2023 14:33:20 GMT  
		Size: 286.1 KB (286088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
