## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:f8d33e8702c1fd370a34334135d75b5bc88c9b2a215cf0eddc88370cd77323d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:17259e9962b7d067be1067ac841d3e477b1b17ae621196a71f7e81cdd2241f12
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec2ca9e9ae74dd07e6d0edffcae867b93166ceba2277589742c3b8ffa0ce7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:24 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da9bd3ea387bd8f0c1d956c5f13bc59105ab662f4faa816279a810b0e41035`  
		Last Modified: Tue, 17 Aug 2021 11:43:48 GMT  
		Size: 6.6 MB (6571669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee3441efbe03819d8184474dc717251fb4974110beca925e6149a15a671513`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 3.2 KB (3156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f8b5792a9dd26b558e699eebf1dbf350b5962108aba91c8e39b2fc3f0be09f`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2b3622754909c2f66abc9b9350ef378d4e0ef9023df1d36ca71d77447da0b`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 292.3 KB (292270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4503ff964929647a79980a1703d4825513e72476336a03949c8edc1a8d33f86d`  
		Last Modified: Tue, 17 Aug 2021 11:43:58 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
