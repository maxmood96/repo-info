## `neurodebian:jessie-non-free`

```console
$ docker pull neurodebian@sha256:82441a0fdf65dfd8310c5389dbdcb8c1d539f6e863bf7434147f68eb83a31132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bed855db832dd322776d1653e9cc1a069c10e1e0d55efd0daa9bf5fa76b941d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54694091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0d95eabf6cfa37a7adf1353f5e8329f06204c20de036827b9003a78d49570d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:21:09 GMT
ADD file:0419e8fcec7ce7e70dc1f1e19558f15ebcd61d43a3b9955811783ac3a56c79ac in / 
# Tue, 09 Jun 2020 01:21:10 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:02:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:03:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Jun 2020 08:03:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Jun 2020 08:05:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:05:35 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:0cd7281e66ed488ba431fd1e41a3c5fd628ed921f059ddbba2597487962ab380`  
		Last Modified: Tue, 09 Jun 2020 01:26:04 GMT  
		Size: 54.4 MB (54388052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163312c76a730419e1a3297a80e03a24565850b98c8f0d136193d9e57e770848`  
		Last Modified: Tue, 09 Jun 2020 08:08:05 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0e1d175494b563dab45371831f57fa5a975f9b95f0f732d3e03d6089c493bb`  
		Last Modified: Tue, 09 Jun 2020 08:08:05 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96f1c35aca839c295bfc8a5f9a033a7e2d5c163e05ddd1bff5fccb6f99543dd`  
		Last Modified: Tue, 09 Jun 2020 08:08:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336098f5fb9f97f0fa0e2f747d4983924776228457613227eb4f9637b25c94d5`  
		Last Modified: Tue, 09 Jun 2020 08:08:05 GMT  
		Size: 302.0 KB (301984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d2dd872e2e3a7a9e39b46a895ad3952bb728d1084a1600eaf0e6e0389670`  
		Last Modified: Tue, 09 Jun 2020 08:08:10 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
