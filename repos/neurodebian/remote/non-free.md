## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:46d4ff0665db7f115a9f18d83aed21a69fbab671f290ae95b4f4e4132518842c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bef51b302becfa096c68984712136aa1f61a955b7ee09a62e025348daa7c6d47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a8a1942392fd5336fbbf0d6ce711a2cbcf599ed6b397b0e79c0714408d7878`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1746f0cf4c2f09051bcb143c8041cfc5033c4d13c9b22a573e8a729923cdf6a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
