## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f514e2e2f40deb64618b63b50b0241adefccd9d681bd5477032fcc15920d6960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:df06a220dad12ff3db9716a50ccdd27e46c3495a55198063f5a39dbd4dfd968c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66556046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935bc8ea0b6e007b340dc3288325b478c79e05012ebffee337d82545b5e24388`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:57:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:57:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 02 Dec 2021 09:57:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 02 Dec 2021 09:57:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:57:11 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2417a2ec45d11420a19842f66e137830a8f5d93c2e607c7af12a819bb7b6094`  
		Last Modified: Thu, 02 Dec 2021 09:59:09 GMT  
		Size: 11.3 MB (11309538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e2ad5320a6bd06e536615ef14f11ed3175dbce8c85b24f3f40d638894d259c`  
		Last Modified: Thu, 02 Dec 2021 09:59:07 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256b7761a93e495588498252f06cf902f493bb4289b83ab2ca0f4cf6323fbe2e`  
		Last Modified: Thu, 02 Dec 2021 09:59:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ab761b0a9f198c380efefcb3244affa3965fdc671c75ddb0f31b27b958e85e`  
		Last Modified: Thu, 02 Dec 2021 09:59:07 GMT  
		Size: 311.3 KB (311255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed781c4f4d6cd509b6245f5f7c89261b13848b65eb9314fdde97bcf57643eb7`  
		Last Modified: Thu, 02 Dec 2021 09:59:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
