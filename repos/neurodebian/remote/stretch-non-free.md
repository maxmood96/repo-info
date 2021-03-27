## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:b02a908cd6816c4ee8f62603a56772dfc00bb4b61cd5deec3e8f6dc26dec6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bb875460f4b314032955092071b6a6fa77cbb87596ce350a66d3c26cea7205ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24e72e9258d6a875fa0086ee783aadfa097793735e3a470df60f377d310d3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:45:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:45:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:45:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:04 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219624edc57f8ae307096765b713cbc6cefdc69fec74c06c78613579cefb7005`  
		Last Modified: Sat, 27 Mar 2021 06:48:21 GMT  
		Size: 6.6 MB (6571660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6115d3a6671264c4594e46054ab582065636218e4e63a8aff8d122275f3d8`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef4b6c402970f4c8ce03bf72d618dca5c1e883e855255f80d2d99d50c79a666`  
		Last Modified: Sat, 27 Mar 2021 06:48:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c8f4ef1f6832be5df5cc7b9bc491a5c5ab0304cdb4281c6f3283d96012072`  
		Last Modified: Sat, 27 Mar 2021 06:48:20 GMT  
		Size: 292.3 KB (292257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf9d19337ea3a2a51e67b71b32f41777ead165cae044e28b505930bbeaad73`  
		Last Modified: Sat, 27 Mar 2021 06:48:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
