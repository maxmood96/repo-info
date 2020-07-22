## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:75adbe27662c88455b80d80182b5d967cd09714f68f98369936202ee746e5b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:29dbcd163970b2acd314f6855f4c735b61864bc589911ebf3390101d7caaa1c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65526693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad82f0dec381ed4ff99e394934f7154dbf08f04def0e4b7fdfc0dd445b20b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:02:39 GMT
ADD file:1fda4c82a4eaecf44b3fc4eb92bb0aac8d81c1c87822bd86f8b52b3620b70420 in / 
# Wed, 22 Jul 2020 02:02:40 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:24:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:24:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 22 Jul 2020 20:24:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 22 Jul 2020 20:24:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:25:07 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:c07b17c5753ba5920876a4091c37318cc0787c8027550cb13d9c1bd7ebfab87f`  
		Last Modified: Wed, 22 Jul 2020 02:09:11 GMT  
		Size: 54.1 MB (54102477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a9bcb0c5e17644ba50441d411ffe2d66f54233859f89083eb8425684f6f9df`  
		Last Modified: Wed, 22 Jul 2020 20:26:45 GMT  
		Size: 11.1 MB (11107223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0290c3823451b2e2c99939b206cf69a6371ea9c2dab4efdfb4ad59f91f525853`  
		Last Modified: Wed, 22 Jul 2020 20:26:42 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dde02736b8d4f4d0b03f544df806e7195384ffc34b11d911f2bb0f7b832aa61`  
		Last Modified: Wed, 22 Jul 2020 20:26:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca0c555087bc9ee4536f26f667c6e9aea24ad75e7e7cd005c209313c191c00`  
		Last Modified: Wed, 22 Jul 2020 20:26:42 GMT  
		Size: 314.7 KB (314664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5494df4de9f19506e4b53d36fa995532c660c5560bae649d79267964d04ceb53`  
		Last Modified: Wed, 22 Jul 2020 20:26:49 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
