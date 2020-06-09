## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:8928914e2b8e01c6f2ba7ef77c628219e2a0841acbf1bffc01232d4a5ae1d94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c3d243f0688b1ab486936ac378065af7e1c174b9fd1b587b6d720e373adc6c06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61191771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7a21e2224107e461d30388a0a8dc5b2393d6a46135092a0690020412b45ae6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:06:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:06:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Jun 2020 08:06:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Jun 2020 08:06:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:06:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4679fe5585f69d90db1edd4fd8e51b33f2986367e7dcfd31ba4e5d917ae60037`  
		Last Modified: Tue, 09 Jun 2020 08:08:27 GMT  
		Size: 10.5 MB (10497423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cc979828926423cf90aac0953e26565b8b74ec6c9e675bde1f4af7c2641419`  
		Last Modified: Tue, 09 Jun 2020 08:08:25 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d4d75bd65dc10cfb052a298632377c3c4f43e8712eb082b6ece0440cce21b`  
		Last Modified: Tue, 09 Jun 2020 08:08:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9006d159851462c506869947e99664edc90917929fe6f2ef99a50511c7442`  
		Last Modified: Tue, 09 Jun 2020 08:08:25 GMT  
		Size: 302.5 KB (302474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740d96893b246dcc59aa82aa198b35b2b3160a135fd926c70f216cdae9ecca48`  
		Last Modified: Tue, 09 Jun 2020 08:08:32 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
