## `neurodebian:jessie`

```console
$ docker pull neurodebian@sha256:196f35aeac537e225edbe0dc8b398b715f828ab185f1dac38c75d9c89d0f4817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie` - linux; amd64

```console
$ docker pull neurodebian@sha256:4873284c24614cb9828879a14e635c3f9831c6a46f93f9a3d242baad17749383
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54693725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582964ed70d096727a79e1f65383a3b7fde0f14166b56a52599c95b33442e350`
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
