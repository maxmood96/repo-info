## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:772b0c10003f48bcbbd88acae1e82b299fd4931cc9d931d481f7cbe2bce12eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f3266b3a4778a79cde36999ac63933a863cc7d3c81c38f65d8f1b057e1a626d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31762741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3520b46a7a1d006f014dbc69190af400ac31b7886179ff4a32aba0b27949f7bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 05:27:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:27:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 07 Jan 2022 05:27:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 07 Jan 2022 05:28:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:28:06 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b45d0c0edfa900cc5c9225ec7e78cdb1f6e975098c53c3471d2d093639cf3`  
		Last Modified: Fri, 07 Jan 2022 05:30:12 GMT  
		Size: 4.8 MB (4813704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab7a9e7c8fea3fdc248724187dde13855733f0d267f9a7cf45997eddde4b80`  
		Last Modified: Fri, 07 Jan 2022 05:30:12 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce93bc2934a328f5f13c32c9711bd25458e4ebff12a73e68193de64380055a25`  
		Last Modified: Fri, 07 Jan 2022 05:30:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacca7ad5f406297b8f76c0ea64279e5beaa6499738da243e03f745f5e7370cf`  
		Last Modified: Fri, 07 Jan 2022 05:30:12 GMT  
		Size: 240.4 KB (240361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7834d2ce2b3a6e3b9bc3fde865be7f99c8c348eccd9a660c3886bfdbec59f9`  
		Last Modified: Fri, 07 Jan 2022 05:30:21 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
