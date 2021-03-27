## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:ca376ab717fc9ca7a9bdb361a6edb6ebcc20426db5f042fd3062df9df5c01a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:167a22f317623d6cbfb5c56ffae7ad083512ce4a16a338f7752e5c93f2dbe399
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61205332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1962dde500ab6b345fd947e1aab221ec5319859b49ae1e0b99ebcd9833b646`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a64e1f4b60995fac7bd8a65ddcc94f637ced0ed4662fa7d8ffa3ca8947238`  
		Last Modified: Sat, 27 Mar 2021 06:48:44 GMT  
		Size: 10.5 MB (10499932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500ee5393cea56c36ff618c71cb990c7f140aec2ca0061e96ac96250bef0e0c`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5bb07b57b9524913e9c7d15292dfd3f125836f353facc7e7934a8dd647db6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a585715510bbe7dc1a5499fbed076b9886c6e83b5b8dca19614ae03984ceec6`  
		Last Modified: Sat, 27 Mar 2021 06:48:42 GMT  
		Size: 302.8 KB (302751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474336b7160442315e21450ba11dc70cd1a99451f34b64e60122100ec3e80ddf`  
		Last Modified: Sat, 27 Mar 2021 06:48:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
