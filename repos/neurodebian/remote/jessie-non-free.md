## `neurodebian:jessie-non-free`

```console
$ docker pull neurodebian@sha256:81b1650aa5060488a1f38af90667a2d8fa6af1aad269d89c14694264e93b724d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9f001a08e48d718ab359b651fe53f05f24270cd02ef53c9175ee57cf0fcf3760
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54697747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f358fca443625c52b696fa2d328985d0d29ebbbf0910a39b081c566adec09`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:29:14 GMT
ADD file:e2991f3845275348c69ea6ada5b84ab1607a345d096ad349fccd010c365a4ebe in / 
# Fri, 15 May 2020 06:29:14 GMT
CMD ["bash"]
# Fri, 15 May 2020 09:14:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:14:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 15 May 2020 09:14:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 15 May 2020 09:16:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:16:51 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:34656812d18fa35ccd0e5b0a4b845092186ee2084e4890153e6a4b84c9efce5f`  
		Last Modified: Fri, 15 May 2020 06:37:58 GMT  
		Size: 54.4 MB (54391709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56e553e219f121d6a2fed10f8fcc9815bdef83f52f4fa37bde0cce9f5bd7a45`  
		Last Modified: Fri, 15 May 2020 09:19:52 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2804fda6e6bf5bdfd9b6381ee1e59e4b006d63c8586cbb41b67960a359b62`  
		Last Modified: Fri, 15 May 2020 09:19:52 GMT  
		Size: 3.2 KB (3153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed8e4c8f72781450ba795b30ba8fba924091fa05c34d9635ecc8b59259449e`  
		Last Modified: Fri, 15 May 2020 09:19:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def2864263b09a517c843ea936ef1fc920405699fe8c44aa2ff58cef9fdbe03`  
		Last Modified: Fri, 15 May 2020 09:19:52 GMT  
		Size: 302.0 KB (301984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bef9d94018811daa92bf63dd831e259be734dc3702a90ae9ba0d05956aa694`  
		Last Modified: Fri, 15 May 2020 09:19:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
