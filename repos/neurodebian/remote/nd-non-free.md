## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ed5ff94e0323eedaf05762e236245597f38a817521efdcdbb7df9ec408cbed33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b4f4b0c0964ad28188cff80b432a4f4cb5777995231c11af07289c52054a4b26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63837196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eb61ede6344ad1d599ba8c8c03a743ba050afe36f8a5d8adb674d4f9ba963b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:02 GMT
ADD file:d09d72986a18210fc325abfbe18d3d35fef6de8ede47304410bea7528e5ab5e6 in / 
# Thu, 10 Sep 2020 00:28:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:31:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:31:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:31:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:12 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5da2bf34dd483faff62b98f29a31447619812af8afb0cdee07c188e866571393`  
		Last Modified: Thu, 10 Sep 2020 00:35:58 GMT  
		Size: 52.5 MB (52488092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cd45687a8a6ce479d5ed7baeba7f25872e2269bae55597a8d89a5a2789a3`  
		Last Modified: Thu, 10 Sep 2020 12:32:23 GMT  
		Size: 11.0 MB (11048048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4eefd16cac44fe531009a5853e37995d9daf8922fe32da710c6a40e83dba2`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539dda8df2b6367d15d7441b7c8e85849646c793b8e0c67cb4db03e5dd7c781`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5f58fe39a0a8c59dc1b8bf17d41f71a4b7da57483daa2bcd9805979b96103`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 298.7 KB (298739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6bdeaee5f394266f8545c56a12b233deeecf728b54f99ae287c1f257c1ea4b`  
		Last Modified: Thu, 10 Sep 2020 12:32:27 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
