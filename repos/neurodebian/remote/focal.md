## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:6a96fcac7a920a5ce3c06b091c642211cd75fbe03551b45c2f4ecf231eecd901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:1dd05450b30c58f1973d6fe1e6fd83ea0d506e1b7c151fbb9760b0139b9ee68b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34292839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4ab851ca848bfa9da5bb5a7daba4279e1f8c5e5f45c84c6b82700cf2e9dd19`
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
