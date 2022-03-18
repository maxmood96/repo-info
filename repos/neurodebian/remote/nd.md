## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:ccea1662fe9f22ebeb8004edabf1bcfcd02c260b3a365f3bb4117fe1d836c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:297460e2945c00d57e88ddf9d1c6db065ed8f24ebdf8cd614708c320464255d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df9c2bc96bce88be296b8467626e67880626f7769cccc6db72524fa0fb439ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:15:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:15:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:15:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128aac36dac7e03aa34a5c0e125dfcec841942698bf8aef01012ee2f596a8d8`  
		Last Modified: Fri, 18 Mar 2022 08:18:41 GMT  
		Size: 11.4 MB (11374011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a999bb7dcc545cc51773d4c7aab4a9bc7f387800fe7ff8f40d0aee6f60935a94`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2eaf0fa50faf1fc453bdf807f0e1a9494babfceea5a2e064bb97c9388c1d6`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe8889081ee40a2d3cf24eb140b00e5f18e6b538f091c567f4aabc0120f07e`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 307.7 KB (307730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
