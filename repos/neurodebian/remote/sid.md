## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:75a438ac96e73f356afa5cafa58fe691d32e91a6d86f77636b3f22c20885a644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:f15491cae08ffbbc478ba82e1b0f3856719e9f89d0eee96a50498e73c88f828c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63794621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c84852d5c9eea53d3d63c12e1b09b4e4300b424f895596a42594135ec19e39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:44:34 GMT
ADD file:7b4df5810238cdff80845df3de1b017b9646e41ae4981a0dc81447c9e63b2e43 in / 
# Tue, 04 Aug 2020 15:44:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:07:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:08:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Aug 2020 23:08:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Aug 2020 23:08:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb43504b07c3311fd407398c6de1b3b659cd4413087291e081d599040a320054`  
		Last Modified: Tue, 04 Aug 2020 15:51:13 GMT  
		Size: 52.4 MB (52403508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e4cfea027e39ce9f4c5b6a7dddbeb1839fba57ffb019fb6ea18fbadae08370`  
		Last Modified: Tue, 04 Aug 2020 23:09:05 GMT  
		Size: 11.1 MB (11090214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c8cdc788c21eb30c107b1c7a934ccd843e60c345e499af01227d0a097426f6`  
		Last Modified: Tue, 04 Aug 2020 23:09:01 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6b803e3f32ea39c3faf24d790c5b28e5350c4080c6b013421ce5522e959696`  
		Last Modified: Tue, 04 Aug 2020 23:09:01 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7336547cb60477ae75727d52775ce81a402c9e779c9a8cb0103c7c286b3f2383`  
		Last Modified: Tue, 04 Aug 2020 23:09:01 GMT  
		Size: 298.9 KB (298900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
