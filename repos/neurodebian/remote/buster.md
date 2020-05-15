## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:b497aca492e7e24165f0e9779766786f7bb250a97fc87c0c68fa8e71147f839f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:566afbe693e83997ec09c53dda41a6b3e09832197b84866706c42a7a1d85b63d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61193238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80820aaaf8f8db1f3b1a20591aeba10bf21258da11eb926cc349ecb9f76abaa0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:28:12 GMT
ADD file:fb54c709daa205bf9d04eb3d90ba068db4c34dfe3b6ec0d7691f677286120903 in / 
# Fri, 15 May 2020 06:28:13 GMT
CMD ["bash"]
# Fri, 15 May 2020 09:17:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:17:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 15 May 2020 09:17:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 15 May 2020 09:17:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:376057ac6fa17f65688c56977118e2e764b27c348b3f70637fa829cd2a12b200`  
		Last Modified: Fri, 15 May 2020 06:37:20 GMT  
		Size: 50.4 MB (50391294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffceaeab4ea69f65a9e881a258f3a8ae6770fcd77610877c1a5fc3a877db69b`  
		Last Modified: Fri, 15 May 2020 09:20:10 GMT  
		Size: 10.5 MB (10497426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c13fe6ffdb339ae946e73a2f24a33fe267fe496f3e7a38db92e79cd2f8e`  
		Last Modified: Fri, 15 May 2020 09:20:08 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793205ed730ad7dfd0fae227428eb9c6889b7a6f4496e46e4a243118c7037f0d`  
		Last Modified: Fri, 15 May 2020 09:20:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232cbc00ce088b6077657d9500766659afcd283b150994ab46cbe30b77bdcc5f`  
		Last Modified: Fri, 15 May 2020 09:20:08 GMT  
		Size: 302.5 KB (302511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
