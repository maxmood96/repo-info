## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:bc0c39aae86597def0f27272b2af65ebfb2a3ff877f39260caa95adc57f75727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:883c47ac6a8575a1c24758747419c7dfc9bfa63d851681293b8bf1aeae1e0b97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf847e6fb8d6afdf487f58c8abd7bc69ca58a9f16dd4f10643c9da5332728bdf`
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
# Fri, 18 Mar 2022 08:15:20 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
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
	-	`sha256:47ebcdd130a728f8e1585d398f32840253f3e7aa5b9beba3b1023d239433e0e0`  
		Last Modified: Fri, 18 Mar 2022 08:18:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
