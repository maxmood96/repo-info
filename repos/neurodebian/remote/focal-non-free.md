## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:03884b4584c9ae1155eec26e6cb7e3e80fb0b346fc6b9671c6f7c6a937024801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:cf3e208f3fed1330d65cbd9e7f5f2ca9fd9e1341ebe83c332d43b85b416d9677
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34293094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d6b42e905bb4ba5ca0ab3a5e64b5eb0b103a9c5c378ca078b9cd8c74adb82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 07:55:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 07:55:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 02 Feb 2022 07:55:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 02 Feb 2022 07:56:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 07:56:08 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96194fea4231911d3e32ebb98343c521e3eba4078e018c32bfbb984bcd789fb2`  
		Last Modified: Wed, 02 Feb 2022 07:59:03 GMT  
		Size: 5.5 MB (5488705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12593dff95b865dc042b774b8c5a1a83a8253918ead6ca4bf65161ecbb961a0`  
		Last Modified: Wed, 02 Feb 2022 07:59:01 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28872c4c80c02e9502f2ac8e43ef2e664328c134125d78b20a5d9447cef5ef8`  
		Last Modified: Wed, 02 Feb 2022 07:59:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c2072fe06c627ed20e89a732ec856db90f5b9b2cc3f9c9c8ea0575af3622c5`  
		Last Modified: Wed, 02 Feb 2022 07:59:02 GMT  
		Size: 238.0 KB (238020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e83d1bb0fdd2c741d458865ce16924a5f9c454c65935f9fdc74bd9ed665d2`  
		Last Modified: Wed, 02 Feb 2022 07:59:12 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
