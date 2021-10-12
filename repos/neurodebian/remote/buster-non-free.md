## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:96018b402a5cffcf8851f46333c55a101e8f05893b342aa6f36fe945a9804300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7c3242ddfa748f44638d535c89fca86b8ec678f14000734c75e375993aa59b60
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a194f50c54fd03797f2187163211189b4ac226997a7bd115046de49f8586c69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:57:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:57:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Oct 2021 09:57:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Oct 2021 09:57:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:58:02 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e876e525a80ef74cc643cd5dfdce86873f4215b425f89e6e69f00b8903f890c`  
		Last Modified: Tue, 12 Oct 2021 09:59:53 GMT  
		Size: 10.5 MB (10500061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623bb473dcd8a6c70699711e22b475a00c294beb830f8134d970244adcdf4131`  
		Last Modified: Tue, 12 Oct 2021 09:59:52 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8670017aa145ab2d3b5d51af1c721f81e31ce8445741a23e4ef654673be1fcc`  
		Last Modified: Tue, 12 Oct 2021 09:59:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6ca2262b5c40c47ef28aa8c673dfc3fc750c562d659034eb5b576c97b1af5`  
		Last Modified: Tue, 12 Oct 2021 09:59:52 GMT  
		Size: 302.8 KB (302769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6283c7f7c67855cd8e3b00f3ae32cf25e3d2368b6a5911c8fa456e999503e21`  
		Last Modified: Tue, 12 Oct 2021 10:00:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
