## `neurodebian:jessie-non-free`

```console
$ docker pull neurodebian@sha256:7146b3913d71bd269aa1dc7975f62a1d05ff94309a3a234ce1b0c7ec0a0b451c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c58d3531fa67f8efb90ba258d60c38ab725863917b19a6b017bfdd8c0f9b6a39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54695003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d6ab54d9fe62ee2ba21831d0bd9184b284a995299b4cd5c0284f9c3ead82d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:43:06 GMT
ADD file:a61ca6a505588ee78f2081330a8a63845fa77b0806553ed8187a6d2b86d1bdbc in / 
# Tue, 04 Aug 2020 15:43:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:04:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:04:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Aug 2020 23:04:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Aug 2020 23:06:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:06:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:27b202087ad6eb0cc07426d7057f407d607e50e7db5f308144da4b7aff31fb0b`  
		Last Modified: Tue, 04 Aug 2020 15:49:29 GMT  
		Size: 54.4 MB (54388987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e059c195dc1a365976632ccbd4264cd1a1f40decae712fb7f0b988f5a3da5`  
		Last Modified: Tue, 04 Aug 2020 23:08:29 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1b65151fd15866ddaf3f134b93d7bd1980b9eb7b276c86aa686810c383f9a3`  
		Last Modified: Tue, 04 Aug 2020 23:08:29 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295193d89c8957a4b0b41f09ac98804cc6399e8214049574ec9587dcb0ddbff0`  
		Last Modified: Tue, 04 Aug 2020 23:08:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09230798bd3f0ec5f3ec077c5ffa13b55b8ff4f193716cc9bfb9f838c1df53`  
		Last Modified: Tue, 04 Aug 2020 23:08:30 GMT  
		Size: 302.0 KB (301957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdbb6d92bc0279227123b98857ce758eb5dc84f387b978052776b948211eab0`  
		Last Modified: Tue, 04 Aug 2020 23:08:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
