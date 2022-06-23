## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:3d8be605756acb409777246f7cdaa4da3008aaaff1ac13cfa684bc93838d08d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:478ed23d2dd19dd3ac4f421e8a2231096e50627a80dc5f4a984adc08c657f56c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66633887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded51f3bdd88b9e79daf8ed0a340e602e694864d7d0f8fe97d3fa06b420074d4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:16 GMT
ADD file:798015650079cb88614ff181a30f9c3d3fde8361c49ae2dec2058d5a3e61f5df in / 
# Thu, 23 Jun 2022 00:20:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:09:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:09:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Jun 2022 04:09:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Jun 2022 04:09:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:09:51 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1339eaac5b67d16d6d9f41fb7a7b96f7cebf3ba4beab36cbb60935aa772af583`  
		Last Modified: Thu, 23 Jun 2022 00:24:48 GMT  
		Size: 55.0 MB (55009886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b08bdfc6193098c58848a110f5b02fee6d817b916b9360742157bfb001f417`  
		Last Modified: Thu, 23 Jun 2022 04:11:54 GMT  
		Size: 11.3 MB (11310328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88896c5fb316c6628a418359707db13e02f747de53ca0b95d7cfd6948ac778a2`  
		Last Modified: Thu, 23 Jun 2022 04:11:53 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5cdd31867d32110b55d16c938e86de05c6aa0e6193502db6bac57096799438`  
		Last Modified: Thu, 23 Jun 2022 04:11:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e09e89565e2ec995a7277d565e8a925d8b2dce8f756fb5f6ba00e023fc80321`  
		Last Modified: Thu, 23 Jun 2022 04:11:53 GMT  
		Size: 311.3 KB (311299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ce94b58fdf145622a02ac2b30f2fd0fed39bcd59091cfe738af7ac072404f9`  
		Last Modified: Thu, 23 Jun 2022 04:12:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
