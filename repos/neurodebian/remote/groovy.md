## `neurodebian:groovy`

```console
$ docker pull neurodebian@sha256:090efcfb55416806d54555bbb34d58931cd84d2cb3434f59e14692e634553187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:groovy` - linux; amd64

```console
$ docker pull neurodebian@sha256:d2b9e74a37481daeea48dbfd068332c52ea2f00409d99ad31a4e6d082813fc8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb0425f6d5672b1459a2513346efe4d6d883c4ab4b1788c4f0cac04baf61f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:47 GMT
ADD file:23ff7ae476ddf97e5dbaf417c06418ae4d8d49a88acb92738bf03fb4a22eeca3 in / 
# Mon, 26 Jul 2021 21:21:47 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:14:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:14:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:14:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:14:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32f3531c8415258308e8d8dda886004bc90cdf4793f9b97c6f33e7903036294f`  
		Last Modified: Mon, 26 Jul 2021 21:23:27 GMT  
		Size: 31.3 MB (31342970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7590a3236a3c9077f44745afe055f10e02d7ded3f4215e2d0d6cb8518f6bb776`  
		Last Modified: Tue, 27 Jul 2021 00:17:58 GMT  
		Size: 5.6 MB (5596499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff8199e15778001f53f30a839e7522b5f4f25d383e1a2ea03a9a4243dcf99f2`  
		Last Modified: Tue, 27 Jul 2021 00:17:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12267d02c4d7623889e5074a4d341ab6eaa6edb500eddc62a83430fa94a5cca7`  
		Last Modified: Tue, 27 Jul 2021 00:17:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcea103f7db3174b9b99fd92d76100a52bad24a862e66fe23241a7cd252ff273`  
		Last Modified: Tue, 27 Jul 2021 00:17:57 GMT  
		Size: 255.5 KB (255521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
