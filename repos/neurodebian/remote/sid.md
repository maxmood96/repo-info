## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5c0008c6e3b23128b0c8343b619e76971232e0310954c39907848d75183222f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:4890cfe74f2502d16cfe80727b279261b3278d185fab426754352585c18d9afd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67488228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28639ea032259f19219f40ef1ff92b044ec0545c066c92530450ff4e1a0dc16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:23:26 GMT
ADD file:10087b555ac457b6a577fbbc8206355ac696e76dd49ff2a4eeeb27ac8b9f4cec in / 
# Tue, 29 Mar 2022 00:23:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:47:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:48:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 29 Mar 2022 19:48:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 29 Mar 2022 19:48:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48f4b65c158eb45a0eb2daaee21a00efa6f1ed6e8943806281db050162c30174`  
		Last Modified: Tue, 29 Mar 2022 00:29:32 GMT  
		Size: 55.8 MB (55804401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bca967af30daff85beb9c5c308e639f8476f7a94a7e23db428e0fb154ba79`  
		Last Modified: Tue, 29 Mar 2022 19:50:25 GMT  
		Size: 11.4 MB (11374186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c340658bf2935196a895a8b65267bca4fc6935d5107807490cf5783d52acf9f`  
		Last Modified: Tue, 29 Mar 2022 19:50:24 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cc648f0b14484865dc37be8572acf4f68c935fe199fc02bde1b65524f51b7c`  
		Last Modified: Tue, 29 Mar 2022 19:50:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6b036332d6fab70960841fd53934d8b71fb37ab79e9cb413acf531c74d8641`  
		Last Modified: Tue, 29 Mar 2022 19:50:24 GMT  
		Size: 307.6 KB (307635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
