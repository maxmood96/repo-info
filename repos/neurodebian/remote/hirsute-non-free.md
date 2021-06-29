## `neurodebian:hirsute-non-free`

```console
$ docker pull neurodebian@sha256:3e2527b1bebb7275be5a6cb17c53896906dd7d40a8c554f1408f1d1dd5cdb8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:hirsute-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4866e57669fb2c6ae41b19cf72da340209562d10a58f336f093fcf25358dd480
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7387c9ae4b70a3e011b0deb60cf79db3d9d4ea77b7bc78fd34a6c54ef4558807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:44 GMT
ADD file:60b287b09986a8e8c3d9cdca2ee7e42ccb5349cca29f8720b7269b258551be15 in / 
# Thu, 17 Jun 2021 23:31:44 GMT
CMD ["bash"]
# Tue, 29 Jun 2021 03:07:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 03:07:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 29 Jun 2021 03:07:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 29 Jun 2021 03:07:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Jun 2021 03:07:47 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:3e2d1c03542857d58a3cae774cad57f863543c683f444da46126220e343c359f`  
		Last Modified: Thu, 17 Jun 2021 23:33:33 GMT  
		Size: 31.8 MB (31838498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb149444cad09521105d665ad0070a877445eb51c1502a3efd9041ebdbdd9a44`  
		Last Modified: Tue, 29 Jun 2021 03:09:03 GMT  
		Size: 5.6 MB (5597791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547f901a9c64b4ff8b34aa4de79f40d37ce911e72672b0e6ab7e390bd0502eb2`  
		Last Modified: Tue, 29 Jun 2021 03:09:01 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c960143c4a8dda2b070622beb279e6eef5936f403f14d7ab5a2202e9c1b2e0`  
		Last Modified: Tue, 29 Jun 2021 03:09:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186fa81be4296305eae22923281d2c5d769b94293d155f66b6ce19146ce9b32c`  
		Last Modified: Tue, 29 Jun 2021 03:09:02 GMT  
		Size: 249.5 KB (249463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c70345fd7bf857202d3b87fe657eba035527f401c6c11a95a93cf4fcc14a83c`  
		Last Modified: Tue, 29 Jun 2021 03:09:12 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
