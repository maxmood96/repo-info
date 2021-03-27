## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5ec46d7f26ae63961dd31c66c24980c8d67a2790b2554c2976c3946c501ff408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:8f1c27c5f380c56971be630eaa17fac9504108e027226c42cfd5720c5068ad6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a3505079e6ec7ccae5c6295ef4ade9339f7e92ef43031933472e7e01797df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:32 GMT
ADD file:2077716d4a510c614acac732f9b9130b649ac696764e3becc6e21e732f39e9c6 in / 
# Fri, 26 Mar 2021 15:22:33 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:47:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:47:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:47:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6db1addbc87ce8e502d75dae59834703a516712298c58eaee03f40a399e8292`  
		Last Modified: Fri, 26 Mar 2021 15:30:40 GMT  
		Size: 54.9 MB (54868141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9eeffb47c540d6fa5caef3fcaa66750050bfd0c116253947d087ecf0ef7a84`  
		Last Modified: Sat, 27 Mar 2021 06:49:37 GMT  
		Size: 11.3 MB (11305751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02159ef5c0b757456dd3da2955f66136688806aee6cddc4e04a5840918df1e`  
		Last Modified: Sat, 27 Mar 2021 06:49:35 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6baa1a0325071f162dcf13db50337fd626e0bbc7daeaba6ca66b3defd7af512`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b1df463008071e0f80383eef835d97ef56cb9dfb77baf28a22387a68c018c`  
		Last Modified: Sat, 27 Mar 2021 06:49:36 GMT  
		Size: 310.6 KB (310649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
