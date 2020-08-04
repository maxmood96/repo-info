## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:b95227933a21d5840e48880e693269fd00f4e772a58f3453fa6a8e367c67c029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f8050a703d42aa97956abb9e2c7052bb6a7c1f7c08ebdada6eb3b39068d0fee7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63794937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869378db2f161d93f211dc7e033e0f079e0b3f16538fcc99e6a946e627cf3bf2`
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
# Tue, 04 Aug 2020 23:08:10 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
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
	-	`sha256:2dccc89c902a648e5d79c8456ba7d6bd2bf5e1b833cd7dda6937824d72cf967a`  
		Last Modified: Tue, 04 Aug 2020 23:09:12 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
