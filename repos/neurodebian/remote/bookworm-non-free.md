## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:15c3e258dfc44a4f0a456f21bdf4771bba5e74aa1ae67ba3b47656ca46d4c4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:439aba25b614e28729b65ec35665431ea8d06c0fa50b72d33cdb4e4c3a206227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64930008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefef3eb581fb00da9c93ef1559a06fdf29d347f0c2629b3ea5ca8d5f43bc4f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:19:54 GMT
ADD file:7e968e6ae38ede120a52f1d2e734b4fee4fd4ffd6e5f747edc8190d2a8bc6a52 in / 
# Thu, 23 Jun 2022 00:19:56 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:10:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:10:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Jun 2022 04:10:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Jun 2022 04:10:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:10:10 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8849e73adf621df4a443e9ac4eec9b698476e4f14f8ed894806f302d5b33156b`  
		Last Modified: Thu, 23 Jun 2022 00:24:12 GMT  
		Size: 53.0 MB (52993983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655051870a5eefa5b208149ef27eef260a9c29d44dce67b3efb83316109809d0`  
		Last Modified: Thu, 23 Jun 2022 04:12:19 GMT  
		Size: 11.6 MB (11642291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444472dd83d067be717ae8cd75a9c4201726ce07daeee2d7868bbacb6ae23669`  
		Last Modified: Thu, 23 Jun 2022 04:12:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d334575459f8aeefe3acc09c65c704817c0dcb21b3b53f0818de93ad7086ab`  
		Last Modified: Thu, 23 Jun 2022 04:12:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c9d72cdf487791ac7a656e8d23becd285468686b97073fe6b58faaebebb944`  
		Last Modified: Thu, 23 Jun 2022 04:12:18 GMT  
		Size: 291.4 KB (291356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ceaeac082ff0a9fba52b0721cd91ed28d3452607a4b1349c53f3adcd90f041`  
		Last Modified: Thu, 23 Jun 2022 04:12:28 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
