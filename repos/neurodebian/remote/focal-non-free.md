## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:839119d3149fdabb9757dba9e8c8d2e4da0f3d6ff2cf67b5235a059bc629bbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:01e7915db023a737a56340dfe2fd95399210a85cc559374bc806d7bf55019d1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34282848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fd1463d4c93e9554eb0926150b053f9b203c8d6b7451fb624faf1139dd84a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:52:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Jun 2021 04:52:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Jun 2021 04:52:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 04:52:49 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4a77e48a4e30ad5b9a0e8f57a8941b5e4afd803b768a118af1f4395e9af730`  
		Last Modified: Fri, 18 Jun 2021 04:55:23 GMT  
		Size: 5.5 MB (5488782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bc8c0b52966c29981f450a633c9e42cd66d2bc21ed88bdbb4bc8725848587c`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c875b70270f67ed702580b6ff4c2fbcb6e07be3081b0884904af67c78aa811f`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0629f8de5ae05b122171d9e1b056f0723c06414eef890d5630081aa0b06dcbe5`  
		Last Modified: Fri, 18 Jun 2021 04:55:22 GMT  
		Size: 238.1 KB (238112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11f19f52782c866f0af53b6f977420b5fce2df64080ac5c2a1c45a7b530a39d`  
		Last Modified: Fri, 18 Jun 2021 04:55:32 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
