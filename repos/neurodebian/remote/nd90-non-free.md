## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:bcc9b4e02a1b7345e302e77e761753e982738106be2c9b038e80d375e987f015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ec561e6cb1b92dde2d29907480dfe4a4d531646ba9442ed9f1cde54a773c2b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52233660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a3b636acbb370d696cd6498c7758246c535d393611aa6e7289d25600a8b256`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:23:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:23:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 22 Jul 2020 20:23:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 22 Jul 2020 20:23:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:24:07 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7126069d6b688f97b5138da4795befc632b1c8e7a43eda9e49b10aa31a7d47`  
		Last Modified: Wed, 22 Jul 2020 20:26:21 GMT  
		Size: 6.6 MB (6568099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12d38e6ac93f683581028e18b24721b8b23157bcc3fbbbe624c143c0c6c0a57`  
		Last Modified: Wed, 22 Jul 2020 20:26:20 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd7782b421963136fc9c96b6c9f77705134c0ce29e07ab28ec02e603b9d70fc`  
		Last Modified: Wed, 22 Jul 2020 20:26:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1c63d9e02cac9cbe2541d7ed9b5fc3f5c9e1c380f953f2b1531d0c778d041a`  
		Last Modified: Wed, 22 Jul 2020 20:26:20 GMT  
		Size: 292.1 KB (292124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9039aacac5f3a47dd5a5cb2d3c0bdc5bac09f135bb0688f005ca35efbbfa7cb5`  
		Last Modified: Wed, 22 Jul 2020 20:26:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
