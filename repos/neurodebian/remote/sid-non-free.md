## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:0d6860e6c00a1b3a10a3d29d07d7dda728b0135fd13389e37056381b308c1c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c49abe73114f83a2c844c2b051c2b5df0adec5b3eea42af95647021ce0339a22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67418077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9811df0fae6e850500961510e24c70b4b4a54ba49fd5474346ad54b1dc4f9e1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:49:37 GMT
ADD file:aa0a8871e20fb4e68758bdebe7ee1e99e982c5e9d2e97b73575b8dcc2ab4adf8 in / 
# Thu, 02 Dec 2021 02:49:37 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:57:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:57:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 02 Dec 2021 09:57:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 02 Dec 2021 09:57:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:57:38 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:af46a953975205f2d7320842b5338767ad3d4aa084267279fc21cdc807374c52`  
		Last Modified: Thu, 02 Dec 2021 02:56:05 GMT  
		Size: 55.7 MB (55746868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d78651f39dd2a2caf2f0fa1e2cd19948ee6c11e3991df1be5f03122ec257d`  
		Last Modified: Thu, 02 Dec 2021 09:59:28 GMT  
		Size: 11.4 MB (11357666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9871abf7bbb80f7e0aadc59db9b35cc0a823c2883d8da0f38df462e7ad50a3`  
		Last Modified: Thu, 02 Dec 2021 09:59:27 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd1b2f180953b09e9ab796415e8ed0f1e69900e29d46596d7eba6bcedfac366`  
		Last Modified: Thu, 02 Dec 2021 09:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289458f108e4279f5598cc1232e90eaaf53efb87c9054e4f59d1bc448bed3105`  
		Last Modified: Thu, 02 Dec 2021 09:59:27 GMT  
		Size: 311.2 KB (311218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53902019dc63f2ac2b3226e5229bce2d1a0547ff2ef421ee213125700bd795e8`  
		Last Modified: Thu, 02 Dec 2021 09:59:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
